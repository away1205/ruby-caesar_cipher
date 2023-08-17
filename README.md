# Caesar Cipher Encryption with Ruby

The `caesar_cipher2` function is a Ruby implementation of the Caesar cipher encryption technique. The Caesar cipher is a simple substitution cipher where each letter in the plaintext is shifted a certain number of places down or up the alphabet.

## Usage

```ruby
def caesar_cipher2(text, shift)
  # Function code here
end

message = "Hello World"
caesar_cipher2(message, 21)
puts message
```

## Function Explanation

The `caesar_cipher2` function takes two arguments: `text` (the plaintext message to be encrypted) and `shift` (the number of positions each letter should be shifted by). It performs the following steps:

1. Iterates through each character in the `text` string.
2. Gets the Unicode code point of the current character using the `ord` method.
3. Determines whether the character is a lowercase or uppercase letter and sets the appropriate bounds (`a` and `z`).
4. Calculates the `rotate` value, which ensures the shift wraps around the alphabet.
5. Shifts the character code by the specified amount and wraps it around the alphabet if needed.
6. Converts the modified character code back to a character using the `chr` method and updates the `text` string.

## Parameters

- `text`: The plaintext message to be encrypted. Can contain both uppercase and lowercase letters, as well as other characters.
- `shift`: The number of positions each letter should be shifted by. Positive values shift the characters to the right, and negative values shift to the left.

## Examples

### Example 1: Encrypting a Message

```ruby
message = "Hello, Caesar!"
caesar_cipher2(message, 3)
puts message
# Output: "Khoor, Fhdvdu!"
```

In this example, the message "Hello, Caesar!" is encrypted using a Caesar cipher with a shift of 3.

### Example 2: Decrypting a Message

Decrypting is achieved by applying a negative shift value.

```ruby
encrypted_message = "Khoor, Fhdvdu!"
caesar_cipher2(encrypted_message, -3)
puts encrypted_message
# Output: "Hello, Caesar!"
```

Here, the encrypted message "Khoor, Fhdvdu!" is decrypted using a shift of -3.

## Notes

- The function preserves the case of letters and leaves non-letter characters unchanged.
- The `caesar_cipher2` function modifies the `text` string directly; make sure to create a copy if the original needs to be preserved.
- This implementation assumes a simple alphabetic shift and does not consider other aspects of security or cryptography.

---
