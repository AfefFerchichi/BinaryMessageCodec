# BinaryMessageCodec

## Requirements
Design and Implement a Simple Binary Message Encoding
Scheme
Design and implement a simple binary message encoding scheme to be used in a signaling protocol. It will be used primarily for passing messages
between peers in a real-time communication application.
For the purpose of this task we assume a simple message model:
A message can contain a variable number of headers, and a binary payload.
The headers are name-value pairs, where both names and values are ASCII-encoded strings.
Header names and values are limited to 1023 bytes (independently).
A message can have max 63 headers.
The message payload is limited to 256 KiB.
You should implement this in one of the following languages: C++, Java, C#, JavaScript, TypeScript, Objective-C or Swift. The API should be something
like the following (example given in Java):

public class Message {
public Map<String, String> headers;
public byte[] payload;
}
public interface MessageCodec {
byte[] encode(Message message);
Message decode(byte[] data);
}

You are expected to motivate the design choices that goes into the encoding scheme you choose to implement.
As an indicator of the scope and (non-)complexity of the encoding scheme that is expected, think of it as that you are expected to be able to
describe the binary message structure on a high-level in a matter of a couple of sentences.
You are expected to design a minimal (in terms of scope / complexity, not necessarily message size) binary encoding scheme that is tailored for
this specific use case.
Do NOT use any platform built-in or third-party serializer implementations.
Keep the implementation simple and in proportion to the complexity of the problem described, i.e. don't overdo it. At the same time, do write
production-grade code w.r.t clean code, input validation and error handling.
