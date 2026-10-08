# Hangman (C++)

C++로 만든 콘솔 행맨 게임입니다. 무작위로 고른 영어 단어를 한 글자씩 추측해 맞히면 됩니다.

## 게임 규칙

- 단어는 `HELLO`, `WORLD`, `COMPUTER`, `PROGRAMMING`, `GAMES` 중 하나가 무작위로 선택됩니다.
- 한 번에 알파벳 한 글자를 입력합니다. 대소문자는 구분하지 않습니다.
- 틀린 글자를 입력하면 기회가 하나 줄어들며, 기회는 총 **6번**입니다.
- 기회가 남아 있을 때 모든 글자를 맞히면 승리, 기회를 다 쓰면 정답이 공개됩니다.
- 한 판이 끝나면 `y`를 입력해 다시 할 수 있습니다.

## 빌드 및 실행

C++11 이상을 지원하는 컴파일러(g++, clang++, MSVC)가 필요합니다.

```bash
g++ -std=c++11 -o hangman Hang_man_using_Cpp.cpp
./hangman
```

Windows(MSVC)에서는 `cl /EHsc Hang_man_using_Cpp.cpp` 후 `Hang_man_using_Cpp.exe`를 실행하세요.

## 실행 예시

```
Guess the word: _____
Enter a letter: o
Guess the word: _O___
Enter a letter: z
Incorrect guess. Attempts left: 5
...
Congratulations! You guessed the word: WORLD
Play Again? (y/n): n
```

## 단어 추가하기

`Hang_man_using_Cpp.cpp` 상단의 `words` 벡터에 **대문자** 단어를 추가하면 됩니다.

```cpp
std::vector<std::string> words = {"HELLO", "WORLD", "COMPUTER", "PROGRAMMING", "GAMES"};
```
