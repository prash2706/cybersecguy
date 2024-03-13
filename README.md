<h1>Project Name </h1>

**Decrypt an encrypted message**

<h2>Description </h2>
In this project I am performing some basic cryptographic activities using Linux commands to decrypt files and reveal hidden messages.

<h3> Scenario </h3>

In this scenario, all of the files in my home directory have been encrypted. I’ll need to use Linux commands to break the Caesar cipher and decrypt the files so that you can read the hidden messages they contain.

Here’s how I’ll do this task: First, I’ll explore the contents of the home directory and read the contents of a file.
Next, I’ll find a hidden file and decrypt the Caesar cipher it contains. Finally, I’ll decrypt the encrypted data file to recover your data and reveal the hidden message.

**Note** the lab starts with I logged in as user analyst, with my home directory, /home/analyst, as the current working directory.

<h4>Task 1. Read the contents of a file</h4>
The lab starts in your home directory, /home/analyst, as the current working directory.

In this task, I need to explore the contents of my home directory and read the contents of a file to get further instructions.

Use the ls command to list the files in the current working directory.
<img width="780" alt="Screenshot 2024-03-12 at 21 38 40" src="https://github.com/prash2706/cybersecguy/assets/85704430/b4e77f50-00ff-4169-82a4-0267bb494410">

2. Use the cat command to list the contents of the README.txt file.

The command to complete this step:

<img width="661" alt="Screenshot 2024-03-12 at 21 39 26" src="https://github.com/prash2706/cybersecguy/assets/85704430/7af51d3d-0889-466e-a67b-356d4b2c959d">

The message in the README.txt file advises that the caesar subdirectory contains a hidden file.

In the next task, I’ll need to find the hidden file and solve the Caesar cipher that protects it. The file contains instructions on how to recover my data.

<h4>Task 2. Find a hidden file</h4>

In this task, you need to find a hidden file in your home directory and decrypt the Caesar cipher it contains. This task will enable you to complete the next task.

First, use the cd command to change to the caesar subdirectory of your home directory:
<img width="682" alt="Screenshot 2024-03-12 at 21 42 05" src="https://github.com/prash2706/cybersecguy/assets/85704430/750b649e-da63-4afa-98e5-647152235a78">

The command to complete this step:

<img width="701" alt="Screenshot 2024-03-12 at 21 42 42" src="https://github.com/prash2706/cybersecguy/assets/85704430/cb9ada3f-5bd4-438f-a6b2-03fe2a2fb0e2">
<img width="717" alt="Screenshot 2024-03-12 at 21 42 54" src="https://github.com/prash2706/cybersecguy/assets/85704430/f1514bd8-9425-4a88-b8d9-b28507f8496d">

Hidden files in Linux can be identified by their name starting with a period (.).

Use the cat command to list the contents of the .leftShift3 file.
The command to complete this step:

<img width="753" alt="Screenshot 2024-03-12 at 21 43 18" src="https://github.com/prash2706/cybersecguy/assets/85704430/eae66cbd-ad0c-441f-84b5-86fe75638def">

The message in the .leftShift3 file appears to be scrambled. This is because the data has been encrypted using a Caesar cipher. 
This cipher can be solved by shifting each alphabet character to the left or right by a fixed number of spaces. In this example, the shift is three letters to the left. Thus "d" stands for "a", and "e" stands for "b".

I  decrypted the Caesar cipher in the .leftshift3 file by using the following command:

<img width="676" alt="Screenshot 2024-03-12 at 21 44 07" src="https://github.com/prash2706/cybersecguy/assets/85704430/82bf7fd8-ce66-4fac-94a1-85e915a6b35e">

In this case, the command tr "d-za-cD-ZA-C" "a-zA-Z" translates all the lowercase and uppercase letters in the alphabet back to their original position. 
The first character set, indicated by "d-za-cD-ZA-C", is translated to the second character set, which is "a-zA-Z".
<img width="743" alt="Screenshot 2024-03-12 at 21 44 46" src="https://github.com/prash2706/cybersecguy/assets/85704430/4ab33163-2904-4162-ba9b-bde0b2416d79">

<h4>Task 3. Decrypt a file</h4>
Now that you have solved the Caesar cipher, in this task you need to use the command revealed in .leftshift3 to decrypt a file and recover your data so you can read the message it contains.

Use the exact command revealed in the previous task to decrypt the encrypted file:
<img width="679" alt="Screenshot 2024-03-12 at 21 45 41" src="https://github.com/prash2706/cybersecguy/assets/85704430/e3fbbba2-bdd1-4f61-aab0-0ea37113a2a4">

Although I don't need to memorize this command, to help better understand the syntax used, let's break it down.

In this instance, the openssl command reverses the encryption of the file with a secure symmetric cipher, as indicated by AES-256-CBC. 
The -pbkdf2 option is used to add extra security to the key, and -a indicates the desired encoding for the output. The -d indicates decrypting, while -in specifies the input file and -out specifies the output file. The -k specifies the password, which in this example is ettubrute.

Use the ls command to list the contents of my current working directory again.
The command to complete this step:
<img width="739" alt="Screenshot 2024-03-12 at 21 46 33" src="https://github.com/prash2706/cybersecguy/assets/85704430/85a590c5-ca93-4936-a976-1fe144599611">






