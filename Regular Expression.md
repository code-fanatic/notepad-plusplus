# Regular Expression - Search
> [!NOTE]  
> Information given below applies to the (Regular Expression Search mode) in npp

## Characters (`letters`, `digits`, `_`)

| **Pattern** | **Description**                                         | **Example Matches**              |
| ----------- | ------------------------------------------------------- | -------------------------------- |
| `\w`        | Matches **1 word character** (`A–Z`, `a–z`, `0–9`, `_`) | `a`, `Z`, `9`, `_`               |
| `\wa`       | Matches **1 word character** followed by `a`            | `aa`, `ba`, `_a`, `1a`           |
| `\waa`      | Matches **1 word character** followed by `aa`           | `aaa`, `baa`, `_aa`, `1aa`       |
| `\wabc`     | Matches **1 word character** followed by `abc`          | `aabc`, `_abc`, `1abc`           |
| `\w\wa`     | Matches **2 word characters** followed by `a`           | `aaa`, `bba`, `_1a`              |
| `\w+`       | Matches **1 or more word characters**                   | `apple`, `b_a_t`, `_cat`, `x`    |
| `\w+e`      | Matches **1 or more word characters ending with `e`**   | `apple`, `_voice`, `drive`, `_e` |
| `a\w+e`     | Matches **starting with `a` and ending with `e`**       | `apple`, `a_b_l_e`, `ace`        |

---

## Digits (`0-9`)

| **Pattern** | **Description**                                   | **Example Matches** |
| ----------- | ------------------------------------------------- | ------------------- |
| `\d`        | Matches **1 digit**                               | `0`, `5`, `9`       |
| `\da`       | Matches **1 digit** followed by `a`               | `1a`, `9a`          |
| `\d\da`     | Matches **2 digits** followed by `a`              | `12a`, `34a`, `55a` |
| `\d+`       | Matches **1 or more digits**                      | `0`, `12`, `345`    |
| `\d+0`      | Matches **digits ending with `0`**                | `10`, `120`, `900`  |
| `0\d+9`     | Matches **starting with `0` and ending with `9`** | `01239`, `009`      |

---

### Whitespace (space, tab, newline)

| **Pattern** | **Description**                                   | **Example Matches** |
| ----------- | ------------------------------------------------- | ------------------- |
| `\s`        | Matches **any whitespace** (space, tab, newline)  | ` `, `\t`, `\n`     |
| `\s+`       | Matches **1 or more whitespace characters**       | `   `, `\n\t`       |
| `\s?`       | Matches **0 or 1 whitespace**                     | ` `, *(none)*       |
| `\S`        | Matches **any non-whitespace character**          | `a`, `1`, `_`, `!`  |
| `\S+`       | Matches **1 or more non-whitespace characters**   | `hello`, `1234`     |
| `\s\S`      | Matches **whitespace followed by non-whitespace** | ` a`, `\n1`         |
| `\S\s`      | Matches **non-whitespace followed by whitespace** | `a `, `1\t`         |


---

### Brackets

| **Pattern** | **Description**                           | **Example Matches** |
| ----------- | ----------------------------------------- | ------------------- |
| `\(` `\)`   | Matches literal **parenthesis**           | `(`, `)`            |
| `\[` `\]`   | Matches literal **square brackets**       | `[`, `]`            |
| `\{` `\}`   | Matches literal **curly braces**          | `{`, `}`            |
| `\(abc\)`   | Matches `abc` **inside parentheses**      | `(abc)`             |
| `(abc)`     | Matches and **captures** `abc`            | `abc`               |
| `[abc]`     | Matches **one of** `a`, `b`, `c`          | `a`, `b`, `c`       |
| `\{abc\}`   | Matches literal `{abc}`                   | `{abc}`             |
| `a{2}`      | Matches **exactly 2** `a`                 | `aa`                |
| `a{4}`      | Matches **exactly 4** `a`                 | `aaaa`              |
| `a{2,}`     | Matches **2 or more** `a`                 | `aa`, `aaa`         |
| `a{4,}`     | Matches **4 or more** `a`                 | `aaaa`, `aaaaa`     |
| `a{2,4}`    | Matches **2 to 4** `a`                    | `aa`, `aaa`, `aaaa` |
| `[a-z]`     | Matches **lowercase letters**             | `a`, `m`, `z`       |
| `[0-9]`     | Matches **digits**                        | `0`, `5`, `9`       |
| `[^abc]`    | Matches **anything except** `a`, `b`, `c` | `0`, `x`, `_`       |
| `(abc)+`    | Matches **one or more `abc`**             | `abc`, `abcabc`     |

---

### Additional Notes:
**Context in Notepad++:**
   - Ensure that you are using "Regular Expression" in the Find/Replace dialogue box.
   - Regex patterns in Notepad++ are case-sensitive.
