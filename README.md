<div id="table-of-contents">
<h2>Table of Contents</h2>
<div id="text-table-of-contents">
<ul>
<li><a href="#org917bf70">1. 開始之前</a></li>
<li><a href="#orgf1bc35b">2. '*'作為大綱、標題亦可視為樹</a></li>
<li><a href="#org321ab94">3. 條列式項目</a></li>
<li><a href="#orgcb99050">4. 文句相關應用</a></li>
<li><a href="#org0966496">5. 超連結範例</a></li>
<li><a href="#org2c62098">6. 顯示圖片範例</a></li>
<li><a href="#org832084b">7. 表格</a></li>
<li><a href="#org60a4bbb">8. 註解(Comments)</a></li>
<li><a href="#org6b7a4a7">9. 標籤(tag)</a></li>
<li><a href="#org7c9293e">10. <span class="todo TODO">TODO</span> and Org-Capture</a></li>
<li><a href="#org1ca835d">11. 記錄做事的時間</a></li>
<li><a href="#org996dac4">12. org-agenda 追蹤狀況</a></li>
<li><a href="#org813987e">13. 插入程式碼</a></li>
<li><a href="#org838aef8">14. 使用 GnuPG 加密內容</a></li>
<li><a href="#org635cec2">15. 輸出</a></li>
<li><a href="#org877bf37">16. 其他</a></li>
</ul>
</div>
</div>


<a id="org917bf70"></a>

# 開始之前

內文敘述中有不少快捷鍵敘述，因此先於開頭定義

當有兩個以上按鍵時，開頭的大寫字母分別表示下列按鍵

-   C : Ctrl
-   M : Alt
-   S : Shift
-   RET : Enter / return

EX: 

-   M-x : Alt + x
-   C-c : Ctrl + c


<a id="orgf1bc35b"></a>

# '\*'作為大綱、標題亦可視為樹

'\*'越多代表層級越低，最多支援到 10 個


<a id="org5bd0cc9"></a>

## 折疊大綱、標題

-   S-TAB 循環切換整個文件的大綱狀態（折疊、打開下一層級、打開全部）
-   TAB 循環折疊或展開光標所在之大綱


<a id="orga4acfa9"></a>

## 大綱、標題間移動

-   C-c C-n/p : 下個大綱/上個標題
-   C-c C-f/b : 前往 下一個同個層級的標題/上一個同個層級的標題
-   C-c C-u : 跳到上一層級標題
-   C-c C-j : 切換為大綱瀏覽狀態


<a id="org652f519"></a>

## 基於大綱、標題的編輯

-   M-RET : 插入同級標題
-   M-S-RET : 插入一個同級TODO標題/於無序條列是則是插入一個帶有複選框的條目
-   M-LEFT/RIGHT : 將此層級標題升級/降級
-   M-UP/DOWN : 將此層級標題上移/下移
-   C-c \* : 將本行設為標題/正文
-   C-c C-w : 將子樹或區域移動到另一標題（可以跨 buffer ）
-   C-x n s/w : 只顯示當前子樹/返回顯示所有樹
-   C-c C-x b : 在新緩衝區顯示當前子樹
-   C-c / : 只列出包含搜尋結果的大綱並且 highlight
-   C-c C-c : 取消 highlight


<a id="orgd237519"></a>

## 關於自動縮排

若想要文件自動縮排可於文件可於文件開頭添加

    #+STARTUP: indent

如果希望打開所有 org 文件都是縮排過的可於 init.el 設定檔中加入以下設定

    (setq org-startup-indented t)


<a id="org321ab94"></a>

# 條列式項目


<a id="org5f52a85"></a>

## 無序條列 :: -,+,\*

-   **這是無序項目一:** 項目定義
-   **這是無序項目二:** 利用 "::" 將描述內容與項目分開
    -   項目二的子項目一
        -   項目二的子項目一的子項目一
    -   項目二的子項目二


<a id="org4ec84c7"></a>

## 有序條列 :: 1. or 1)

1.  這是有序項目一 :: 項目定義
    1.  子項目一
    2.  子項目二
2.  這是有序項目二


<a id="orgcb99050"></a>

# 文句相關應用

-   **粗體**
-   <del>刪除線</del>
-   <span class="underline">畫底線</span>
-   *斜體*
-   `等寬字`
-   `verbatim`
-   e<sup>iπ</sup> + 1 = 0
-   ∑a<sub>n</sub>


<a id="org0966496"></a>

# 超連結範例


<a id="orgfe5a128"></a>

## 一般外部連結

連結直接貼上即可

-   <http://www.google.com>


<a id="org735ad51"></a>

## 文字連結

    [[link address][description]]
    
    [[https://www.gnu.org/software/emacs/][GNU Emacs]]

EX:

-   [GNU Emacs](http://www.gnu.org/software/emacs/)


<a id="org5e4a830"></a>

## 其他連結

-   <file:///Users/ashbeljhuang/.emacs.d/init.el>
-   <somebody@email.net>


<a id="org2c62098"></a>

# 顯示圖片範例

-   輸入檔案所在位置連結 ex: `file:your/image/file/path.xxx`
-   按下 M-x 後，輸入 org-toggle-inline-images 來顯示圖片
-   或著按下 C-c C-x C-v 亦可顯示內容圖片

EX:

    file:org-mode-unicorn-logo.png

![img](org-mode-unicorn-logo.png)


<a id="org832084b"></a>

# 表格

-   使用 | 作為表格分隔
-   TAB 在表格內前往下個內容區域
-   S-TAB 在表格內前往上個內容區域
-   輸入 |- 再按下 TAB 可以在產生分隔線，like: |-&#x2013;&#x2014;+-&#x2013;&#x2014;+-&#x2013;&#x2014;|
-   輸入好欄位標題後按下 C-c RET or C-c | 即可產生表格，差別在於 C-C | 可以再給予列述以及行數
-   表格填入後可以使用 C-c C-c 更新/調整表格
-   C-c ? 可得知該欄位座標資訊, @ 代表(橫)列 $ 代表(直)行, 所以 @2 代表第二列, $3 代表第三行, @1$3 代表第一列第三行的內容

<table border="2" cellspacing="0" cellpadding="6" rules="groups" frame="hsides">


<colgroup>
<col  class="org-left" />

<col  class="org-left" />

<col  class="org-left" />
</colgroup>
<thead>
<tr>
<th scope="col" class="org-left">Mission</th>
<th scope="col" class="org-left">Description</th>
<th scope="col" class="org-left">Deadline</th>
</tr>
</thead>

<tbody>
<tr>
<td class="org-left">Integrate original SDK mission to Offer Wall SDK</td>
<td class="org-left">Research how to integrate original SDK mission to Offer Wall SDK</td>
<td class="org-left">Not yet.</td>
</tr>


<tr>
<td class="org-left">Integrate Appsflyer SDK</td>
<td class="org-left">Integrate Appsflyer SDK to iOS App</td>
<td class="org-left">Not yet.</td>
</tr>


<tr>
<td class="org-left">Localize App</td>
<td class="org-left">Make iOS App localized</td>
<td class="org-left">Not yet.</td>
</tr>
</tbody>
</table>

-   在 #+TBLFM: 可以使用類似試算表或 EXCEL 算式，寫完後使用 C-c C-c (ctrl + c 後 ctrl +c) 更新表格 ex: #+TBLFM: $1 = vmean($1..$2)
-   多個規則或算式則用::分開 ex: #+TBLFM: $1 = vmean($1..$2)::$5 = $3 + $4

<table border="2" cellspacing="0" cellpadding="6" rules="groups" frame="hsides">


<colgroup>
<col  class="org-right" />

<col  class="org-right" />

<col  class="org-right" />

<col  class="org-right" />
</colgroup>
<thead>
<tr>
<th scope="col" class="org-right">Last Month Flow</th>
<th scope="col" class="org-right">This Month Flow</th>
<th scope="col" class="org-right">Two Month Sum Flow</th>
<th scope="col" class="org-right">Month Increment Flow</th>
</tr>
</thead>

<tbody>
<tr>
<td class="org-right">250000</td>
<td class="org-right">300000</td>
<td class="org-right">550000</td>
<td class="org-right">0.2</td>
</tr>


<tr>
<td class="org-right">260000</td>
<td class="org-right">310000</td>
<td class="org-right">570000</td>
<td class="org-right">0.19230769</td>
</tr>


<tr>
<td class="org-right">270000</td>
<td class="org-right">250000</td>
<td class="org-right">520000</td>
<td class="org-right">-0.074074074</td>
</tr>
</tbody>
</table>


<a id="org60a4bbb"></a>

# 註解(Comments)

-   "#" 視為單行的註解
-   使用 C-c ; 註解整個區域
-   在 `#+BEGIN_COMMENT` 以及 `#+END_COMMENT` 中的內文視為註解區域

EX:

    
    # 單行註解不被輸出
    
    #+BEGIN_COMMENT
    指定區塊內不被輸出
    第二行
    第三行
    #+END_COMMENT
    
     **** COMMENT 利用 C-c ; 註解整個區域
     此層級下的內容
     皆不會被輸出


<a id="org6b7a4a7"></a>

# 標籤(tag)

-   在標題使用 C-c C-c 來加上 tag
-   正文中可以使用 C-c C-q 加上 tag
-   tag 具有繼承性，即子標題及其內容會繼承上一層級之標籤
-   C-c \\ 可以尋找某個 tag 下的所有項目
-   C-c / 可以尋找特定的項目，提供多個搜尋方式，EX: m : 桉樹狀結構顯示， / : Regular Expression 搜尋
-   若要整個文件都含有某個標籤，可於文件開頭添加 #+FILETAGS::tag1:tag2:tag3:


<a id="orgb34d677"></a>

## EX: Android     :android:

Android Studio


<a id="orgbbbb5ca"></a>

## EX: iOS     :iOS:MacOS:

XCode


<a id="org8c7cb40"></a>

## EX: Cross Platform     :android:iOS:

-   Xamarin
-   Unity


<a id="org7c9293e"></a>

# and Org-Capture


<a id="orgaeb9311"></a>

## List

-   可以增加其他的設定 ex: #+TODO: TODO(t) WAIT(w@/!) | DONE(d!) CANCELED(c@)
-   使用 S-LEFT / DONE 切換 TODO/DONE/無狀態
-   使用 S-UP / S-DOWN 來增加/減少 priority
-   以 "- [ ]" 開頭的列會被認為是複選框，可以使用 M-S-RET 插入含有複選框之項目
-   使用 M-s RET 增加子項目
-   使用 C-c C-c 改變複選框的狀態
-   使用 C-c C-s 加入日程規劃
-   使用 C-c C-d 加入 deadline


<a id="org0cf3466"></a>

## Org-Capture

常用於記錄臨時想到的事情
於 init.el 檔案中相關設置如下

    ;; Quickly use C-c r to take note
    ;; (global-set-key (kbd "C-c r") 'org-capture)
    
    ;; Setup capture template
    (setq org-capture-templates
    	  '(("t" "TODO" entry (file+headline "" "Tasks") "* TODO %?\n %i\n")
    		("n" "NOTE" entry (file+headline "" "Tasks") "* NOTE %?\n %i\n %a")))

-   M-x org-capture RET 開啟 org-capture 選擇 template 記錄事項


<a id="orgd07acfd"></a>

### EX: Task

1.  TODO work out

2.  DONE buy green tea

3.  TODO TASKS<code>[1/4]</code>

    -   [ ] Integrate origianl SDK mission to Offer Wall SDK
    -   [ ] Integrate Appsflyer SDK to iOS App
    -   [ ] Localize iOS App for multilanguage
    -   [X] Modify gifts redeem to original

4.  TODO Modify gifts redeem to original


<a id="org1ca835d"></a>

# 記錄做事的時間

-   使用 C-c C-x C-i 開始計時
-   使用 C-c C-x C-o 結束計時
-   使用 C-u C-c C-x C-i 來看現在計時


<a id="org996dac4"></a>

# org-agenda 追蹤狀況

-   使用 M-x org-agenda 選擇想要顯示的類型


<a id="org813987e"></a>

# 插入程式碼

如果沒有相關使用需求此段落可跳過


<a id="org070627c"></a>

## Code Generate

-   輸入 <s 後按下 TAB 插入程式碼的樣板
-   使用 C-c ' 編輯程式碼/結束編輯程式碼
-   :exports code / results / both 分別代表文件在匯出時呈現的方式，純 code / 結果 / code加上結果

EX:

    import cgitb
    import json
    
    cgitb.enable()
    
    testJson = {'id': 1, 'firstName': 'Ashbel', 'lastName': 'Jhuang', 'gender': 'male'}
    
    print "Content-Type: text/plain;charset=utf-8"
    print
    print json.dumps(testJson)

-   使用 #+INCLUDE: "file path" 將在他處的檔案包含顯示進來
-   使用 C-c ' 前往 include 的檔案
-   將外部檔案程式碼內容顯示在此文件中 #+INCLUDE: "~/.emacs.d/init.el" src emacs-lisp
-   將外部檔案的內容 19 - 33 行包到此文件中 #+INCLUDE: "~/.emacs.d/init.el" :lines "19-33"
-   將外部檔案的內容到 33 行前包到此文件中 #+INCLUDE: "~/.emacs.d/init.el" :lines "-33"
-   將外部檔案的內容從 19 行開始包到此文件中 #+INCLUDE: "~/.emacs.d/init.el" :lines "19-"

EX:

`#+INCLUDE: "~/.emacs.d/init.el" src emacs-lisp :lines "19-33"`

    ;; some emacs window / buffer settings 
    (setq delete-old-versions t)
    (fset 'yes-or-no-p 'y-or-n-p)
    (prefer-coding-system 'utf-8)
    (tooltip-mode -1)
    (tool-bar-mode -1)
    (menu-bar-mode -1)
    (scroll-bar-mode -1)
    ; (setq visible-bell t)
    (setq column-number-mode 1)
    (global-linum-mode 1)
    (setq-default tab-width 4)
    ; (setq-default indicate-empty-lines t)
    (setq-default show-trailing-whitespace nil)


<a id="org15da6d7"></a>

## Code Evaluate

-   使用 C-c C-c 進行 Code Evaluate
-   使用 M-x org-babel-tangle 產出程式檔案

    echo "Today is $(date)"


<a id="orgcaba9d2"></a>

### ditaa 繪圖

    +------------+
    |            |
    |Hello World!|
    |            |
    +------------+


<a id="org7d8d5b4"></a>

### Graphviz 繪圖

    digraph G{
       {a b c} -> {d e f}
    }


<a id="orgeb25ff8"></a>

### PlantUML

    class Dummy {
      String data
      void methods()
    }
    
    class Flight {
       flightNumber : Integer
       departureTime : Date
    }


<a id="org838aef8"></a>

# 使用 GnuPG 加密內容

如無相關使用需求可跳過此段落


<a id="orgf0e9309"></a>

## 於 init.el 檔案中相關設置如下

注意：請先確認系統有安裝 GnuPG

    ;; crypt
    (require 'org-crypt)
    
    ;; 當被加密的部份要存入硬碟時，自動加密回去
    (org-crypt-use-before-save-magic)
    
    ;; 設定要加密的 tag 標籤為 need_to_encrypt
    (setq org-crypt-tag-matcher "need_to_encrypt")
    
    ;; 避免 need_to_encrypt 這個 tag 被子項目繼承 造成重複加密
    ;; (但是子項目還是會被加密喔)
    (setq org-tags-exclude-from-inheritance (quote ("need_to_encrypt")))
    
    ;; 用於加密的 GPG 金鑰
    ;; 可以設定任何 ID 或是設成 nil 來使用對稱式加密 (symmetric encryption)
    (setq org-crypt-key nil)


<a id="org8288726"></a>

### EX：ID/PW     :need_to_encrypt:

ID: abcdefghij   
PW: 1234567890


<a id="org635cec2"></a>

# 輸出

-   使用 C-c C-e 或 M-x org-export-dispatch RET 呼叫輸出選單
-   使用 C-c C-e # 插入 template


<a id="orgcb74b47"></a>

## 支援的輸出格式

<table border="2" cellspacing="0" cellpadding="6" rules="groups" frame="hsides">


<colgroup>
<col  class="org-left" />

<col  class="org-left" />

<col  class="org-left" />

<col  class="org-left" />
</colgroup>
<thead>
<tr>
<th scope="col" class="org-left">Export Form</th>
<th scope="col" class="org-left">Export Hot Key</th>
<th scope="col" class="org-left">Preview Hot Key</th>
<th scope="col" class="org-left">Remark</th>
</tr>
</thead>

<tbody>
<tr>
<td class="org-left">ASCII</td>
<td class="org-left">&#xa0;</td>
<td class="org-left">&#xa0;</td>
<td class="org-left">&#xa0;</td>
</tr>


<tr>
<td class="org-left">Beamer</td>
<td class="org-left">&#xa0;</td>
<td class="org-left">&#xa0;</td>
<td class="org-left">&#xa0;</td>
</tr>


<tr>
<td class="org-left">HTML</td>
<td class="org-left">C-c C-e h h</td>
<td class="org-left">C-c C-e h H</td>
<td class="org-left">`#+HTML_HEAD`:用來增加 javascript 或是 css, `#+ATTR_HTML`: 可以為 table 或是 src block 增加額外的設置</td>
</tr>


<tr>
<td class="org-left">iCalendar</td>
<td class="org-left">&#xa0;</td>
<td class="org-left">&#xa0;</td>
<td class="org-left">&#xa0;</td>
</tr>


<tr>
<td class="org-left">LaTeX</td>
<td class="org-left">C-c C-e l l</td>
<td class="org-left">C-c C-e l L</td>
<td class="org-left">`#+LATEX_CLASS`: 選擇預先定義好的 LaTeX 樣板, `#+LATEX_HEADER`: 用來增加額外的 LaTeX 套件</td>
</tr>


<tr>
<td class="org-left">Man</td>
<td class="org-left">&#xa0;</td>
<td class="org-left">&#xa0;</td>
<td class="org-left">&#xa0;</td>
</tr>


<tr>
<td class="org-left">Markdown</td>
<td class="org-left">C-c C-e m m</td>
<td class="org-left">C-c C-e m M</td>
<td class="org-left">&#xa0;</td>
</tr>


<tr>
<td class="org-left">ODT</td>
<td class="org-left">&#xa0;</td>
<td class="org-left">&#xa0;</td>
<td class="org-left">&#xa0;</td>
</tr>


<tr>
<td class="org-left">Publishing</td>
<td class="org-left">&#xa0;</td>
<td class="org-left">&#xa0;</td>
<td class="org-left">&#xa0;</td>
</tr>


<tr>
<td class="org-left">Texinfo</td>
<td class="org-left">&#xa0;</td>
<td class="org-left">&#xa0;</td>
<td class="org-left">&#xa0;</td>
</tr>


<tr>
<td class="org-left">Confluence</td>
<td class="org-left">&#xa0;</td>
<td class="org-left">&#xa0;</td>
<td class="org-left">&#xa0;</td>
</tr>


<tr>
<td class="org-left">Deck.js</td>
<td class="org-left">&#xa0;</td>
<td class="org-left">&#xa0;</td>
<td class="org-left">&#xa0;</td>
</tr>


<tr>
<td class="org-left">Freemind</td>
<td class="org-left">&#xa0;</td>
<td class="org-left">&#xa0;</td>
<td class="org-left">&#xa0;</td>
</tr>


<tr>
<td class="org-left">Groff</td>
<td class="org-left">&#xa0;</td>
<td class="org-left">&#xa0;</td>
<td class="org-left">&#xa0;</td>
</tr>


<tr>
<td class="org-left">Koma Scrlttr2</td>
<td class="org-left">&#xa0;</td>
<td class="org-left">&#xa0;</td>
<td class="org-left">&#xa0;</td>
</tr>


<tr>
<td class="org-left">RSS</td>
<td class="org-left">&#xa0;</td>
<td class="org-left">&#xa0;</td>
<td class="org-left">&#xa0;</td>
</tr>


<tr>
<td class="org-left">S5</td>
<td class="org-left">&#xa0;</td>
<td class="org-left">&#xa0;</td>
<td class="org-left">&#xa0;</td>
</tr>


<tr>
<td class="org-left">Taskjuggler</td>
<td class="org-left">&#xa0;</td>
<td class="org-left">&#xa0;</td>
<td class="org-left">&#xa0;</td>
</tr>


<tr>
<td class="org-left">PDF</td>
<td class="org-left">C-c C-e l p</td>
<td class="org-left">&#xa0;</td>
<td class="org-left">&#xa0;</td>
</tr>
</tbody>
</table>


<a id="orgf52fa26"></a>

## 一些關於輸出的參考資料


<a id="org4d56df8"></a>

### HTML5 Slide

-   Epresent: <http://orgmode.org/worg/org-tutorials/non-beamer-presentations.html#sec-2>
-   S5: <http://orgmode.org/worg/org-tutorials/non-beamer-presentations.html#sec-3>
-   org-tree-slide: <http://orgmode.org/worg/org-tutorials/non-beamer-presentations.html#sec-4>
-   org-reveal: <http://orgmode.org/worg/org-tutorials/non-beamer-presentations.html#sec-6>
-   org-ioslide: <https://github.com/coldnew/org-ioslide>


<a id="org99230ad"></a>

### Blogging tools

-   o-blog: <http://renard.github.com/o-blog>
-   Jekyll with org-mode: <http://orgmode.org/worg/org-tutorials/org-jekyll.html>
-   Octopress with org-mode: <https://github.com/tomalexander/orgmode-octopress>
-   Projects: <http://orgmode.org/manual/Publishing.html>
-   Blorgit: <http://orgmode.org/worg/blorgit.html>
-   **org2blog: <https://github.com/punchagan/blog-files>** 大力推薦此工具來撰寫 blog


<a id="org877bf37"></a>

# 其他


<a id="org86961a0"></a>

## 可能會用上的熱鍵

-   c-u c-u c-u TAB 展開所有項目

