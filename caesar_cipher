def encrypt_decrypt(message, shift, operation):
  """Encrypts or decrypts a message using a Caesar cipher with a given shift.

  Args:
    message: The message to encrypt or decrypt.
    shift: The number of positions to shift each letter.
    operation: "encrypt" or "decrypt" to specify the desired operation.

  Returns:
    The encrypted or decrypted message.
  """

  cipher = ""
  for char in message:
    if char.isalpha():
      shift_value = shift if operation == "encrypt" else -shift
      # Shift uppercase letters
      if char.isupper():
        new_char = chr((ord(char) - ord('A') + shift_value) % 26 + ord('A'))
      # Shift lowercase letters
      else:
        new_char = chr((ord(char) - ord('a') + shift_value) % 26 + ord('a'))
    else:
      # Leave non-alphabetic characters unchanged
      new_char = char
    cipher += new_char
  return cipher

# Example usage for encryption
message = "Hello, world!"
shift = 3
encrypted_message = encrypt_decrypt(message, shift, "encrypt")
print(f"Original message: {message}")
print(f"Encrypted message: {encrypted_message}")

# Example usage for decryption
decrypted_message = encrypt_decrypt(encrypted_message, shift, "decrypt")
print(f"Decrypted message: {decrypted_message}")
