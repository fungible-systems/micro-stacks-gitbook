# Message Signing

This page will go over how to sign messages in a react application. To learn more about the underlying functions used, please check out this page:

{% content-ref url="../../core/connect/message-signing.md" %}
[message-signing.md](../../core/connect/message-signing.md)
{% endcontent-ref %}

### useSignMessage

This is the primary hook you'll want to use if you're interested in signing a string payload that is not Clarity code. This can be anything, from a simple string message, to something more complex. If you're looking to sign Structured Data, please check out the next hook.

```jsx
const MyComponent = () => {
  const { handleSignMessage, isLoading } = useSignMessage();
  const { verifyMessageSignature } = useVerifyMessage();

  // to save the data from the wallet
  const [payload, setPayload] = useState(null);
  const [verification, setVerification] = useState(null);
  const [message, setMessage] = useState("");

  const onClick = useCallback(async () => {
    await handleSignMessage({
      message,
      onFinish(p) {
        setPayload(p);
        // verify the payload
        setVerification(verifyMessageSignature(message, p.signature));
      },
    });
  }, [message]);

  return (
    <div
      style={{
        display: "grid",
        gap: "20px",
      }}
    >
      <h5>Sign a message!</h5>
      <input
        style={{ display: "block" }}
        onChange={(e) => setMessage(e.currentTarget.value)}
      />
      <button onClick={onClick}>
        {isLoading ? "Loading..." : "Sign message"}
      </button>
      <code>
        <pre>{JSON.stringify(payload, null, 2)}</pre>
      </code>
      <code>
        <pre>{JSON.stringify(verification, null, 2)}</pre>
      </code>
    </div>
  );
};
```

### useSignStructuredData

This method will accept a hex encoded clarity value, or a `ClarityValue`. Check out the page on Clarity Values to learn more about them:

{% content-ref url="../../core/clarity/clarity-values.md" %}
[clarity-values.md](../../core/clarity/clarity-values.md)
{% endcontent-ref %}

```jsx
const MyComponent = () => {
  const { handleSignStructuredData, isLoading } = useSignStructuredData();
  const { verifyMessageSignature } = useVerifyMessage();

  // to save the data from the wallet
  const [payload, setPayload] = useState(null);
  const [verification, setVerification] = useState(null);
  const [message, setMessage] = useState("");

  const onClick = useCallback(async () => {
    await handleSignStructuredData({
      // note the clarity value
      message: stringAsciiCV(message),
      onFinish(p) {
        setPayload(p);
        // verify the payload
        setVerification(verifyMessageSignature(message, p.signature));
      },
    });
  }, [message]);

  return (
    <div
      style={{
        display: "grid",
        gap: "20px",
      }}
    >
      <h5>Sign a clarity string message!</h5>
      <input
        style={{ display: "block" }}
        onChange={(e) => setMessage(e.currentTarget.value)}
      />
      <button onClick={onClick}>
        {isLoading ? "Loading..." : "Sign message"}
      </button>
      <code>
        <pre>{JSON.stringify(payload, null, 2)}</pre>
      </code>
      <code>
        <pre>{JSON.stringify(verification, null, 2)}</pre>
      </code>
    </div>
  );
};ty
```
