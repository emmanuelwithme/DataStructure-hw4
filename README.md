# 作業三(接續上一次作業)
假定`scores.txt`檔案為500位考生的考試成績,每行資料依序為學號,國文,英文,數學.

1. 請設計Student類別, 可載入所有同學成績,到一個物件陣列, 計算每位考生總分並列印出來.

2. 請將所有同學依(a)總分、(b)國文、(c)英文、(d)數學 之優先順序進行排序, 印出排序結果.(若總分一樣則先比較國文成績，國文成績又一樣則再比較英文成績，英文成績又一樣最後才比較數學成績，所以只會有一種結果，而不是分別用總分、國文、英文、數學排序的四種結果)

提示: 可使用`Arrays.sort`排序物件陣列, 以`Comparator`指定兩物件比較方法

# 作業四(這次作業)
請完成作業三的後續分發問題:
依照成績高低順序,高分者優先選擇志願.
最多錄取一間學校，志願序越前面的優先錄取。
school.txt是十所學校的錄取名額
wish.txt是各考生選填志願序列(0代表終止符號)
1. 請分別印出十所學校的錄取考生編號
2. 請印出沒有錄取任何學校的考生編號
3. 請將所有考生的編號,總分, 志願序與錄取學校號碼印出

**作業比較難，延後到 12/1(日) 晚上23:59前交都不算遲交。**
**請按照我的格式輸出，印出來或存檔都可以(選一即可)，需要一模一樣。**
對應第一小題: 十所學校的錄取考生編號 `output/all_school.txt`
第二小題: 沒有錄取任何學校的考生編號 `output/unassigned_students_ids.txt`
第三小題: 所有考生的編號, 總分與錄取學校編號 `output/all_students.txt`
答對一題80，2題90，3題100。

## 按照上次的要求程式碼要有Student類別，請使用我給的屬性及toString():

    // 學生類別，屬性有: 學號(id)、國文(chinese)、英文(english)、數學(math)、總分(total)、志願序(wishList)、錄取學校編號(schoolId)

    String id;

    int chinese;

    int english;

    int math;

    int total;

    LinkedList<String> wishList;

    String schoolId;

    @Override
    public String toString() {
        return "學號: " + id + ", 國文: " + chinese + ", 英文: " + english + ", 數學: " + math + ", 總分: " + total + ", 志願序: " + wishList + ", 錄取學校: " + schoolId;
    }

## 這次新增School類別，請使用我給的屬性、toString()
    // 屬性有編號(id)、學生名額(quota)、錄取學生學號(studentList)
    String id;
    int quota;
    LinkedList<String> studentList;

    @Override
    public String toString() {
        return "學校編號: " + id + ", 學生名額: " + quota + ", 學生學號: " + studentList;
    }