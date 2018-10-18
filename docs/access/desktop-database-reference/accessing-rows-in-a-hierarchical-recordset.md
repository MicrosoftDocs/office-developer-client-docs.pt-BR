---
<span data-ttu-id="b1553-101"><<<<<<< Título cabeça: acessando linhas em uma TOCTitle de Recordset hierárquico: acessando linhas em um Recordset hierárquico de ms:assetid: db59b152-b780-539c-17ef-462e8adfb26e ms:mtpsurl: https://msdn.microsoft.com/library/JJ250106(v=office.15) ms:contentKeyID: ms.date 48548104: 09/18 / mtps_version 2015: v=office.15</span><span class="sxs-lookup"><span data-stu-id="b1553-101"><<<<<<< HEAD title: Accessing Rows in a Hierarchical Recordset TOCTitle: Accessing Rows in a Hierarchical Recordset ms:assetid: db59b152-b780-539c-17ef-462e8adfb26e ms:mtpsurl: https://msdn.microsoft.com/library/JJ250106(v=office.15) ms:contentKeyID: 48548104 ms.date: 09/18/2015 mtps_version: v=office.15</span></span>
---

# <a name="accessing-rows-in-a-hierarchical-recordset"></a><span data-ttu-id="b1553-102">Acessando as linhas em um conjunto de registros hierárquico</span><span class="sxs-lookup"><span data-stu-id="b1553-102">Accessing Rows in a Hierarchical Recordset</span></span>

<span data-ttu-id="b1553-103">=== título: acessando as linhas em um hierárquico Recordset TOCTitle: acessando as linhas em uma ms:assetid de Recordset hierárquico: db59b152-b780-539c-17ef-462e8adfb26e ms:mtpsurl: https://msdn.microsoft.com/library/JJ250106(v=office.15) ms:contentKeyID: ms.date 48548104: 10/17/2018 mtps_version: v = Office.15</span><span class="sxs-lookup"><span data-stu-id="b1553-103">======= title: Accessing rows in a hierarchical Recordset TOCTitle: Accessing rows in a hierarchical Recordset ms:assetid: db59b152-b780-539c-17ef-462e8adfb26e ms:mtpsurl: https://msdn.microsoft.com/library/JJ250106(v=office.15) ms:contentKeyID: 48548104 ms.date: 10/17/2018 mtps_version: v=office.15</span></span>
---

# <a name="accessing-rows-in-a-hierarchical-recordset"></a><span data-ttu-id="b1553-104">Acessando as linhas em um Recordset hierárquico</span><span class="sxs-lookup"><span data-stu-id="b1553-104">Accessing rows in a hierarchical Recordset</span></span>
>>>>>>> <span data-ttu-id="b1553-105">mestre</span><span class="sxs-lookup"><span data-stu-id="b1553-105">master</span></span>

<span data-ttu-id="b1553-106">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="b1553-106">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="b1553-107">O exemplo a seguir mostra as etapas necessárias para acessar as linhas em um [Recordset](recordset-object-ado.md) hierárquico:</span><span class="sxs-lookup"><span data-stu-id="b1553-107">The following example shows the steps necessary to access rows in a hierarchical [Recordset](recordset-object-ado.md):</span></span>

<span data-ttu-id="b1553-108"><<<<<<< Cabeça</span><span class="sxs-lookup"><span data-stu-id="b1553-108"><<<<<<< HEAD</span></span>
1.  <span data-ttu-id="b1553-109">Os objetos **Recordset** dos autores e as tabelas do autor de títulos são relacionados pelo ID do autor.</span><span class="sxs-lookup"><span data-stu-id="b1553-109">**Recordset** objects from the authors and titleauthor tables are related by author ID.</span></span>

2.  <span data-ttu-id="b1553-110">O loop externo exibe o nome e sobrenome de cada autor, o estado e a identificação.</span><span class="sxs-lookup"><span data-stu-id="b1553-110">The outer loop displays each author's first and last name, state, and identification.</span></span>

3.  <span data-ttu-id="b1553-111">O **Recordset** anexado para cada linha é recuperado da coleção **Fields** e designado ao *rstTitleAuthor*.</span><span class="sxs-lookup"><span data-stu-id="b1553-111">The appended **Recordset** for each row is retrieved from the **Fields** collection and assigned to *rstTitleAuthor*.</span></span>

4.  <span data-ttu-id="b1553-112">O loop interno exibe quatro campos de cada linha no **Recordset** anexado.</span><span class="sxs-lookup"><span data-stu-id="b1553-112">The inner loop displays four fields from each row in the appended **Recordset**.</span></span>

<a name="the-stayinsyncstayinsync-property-adomd-property-is-set-to-false-for-purposes-of-illustration--so-you-can-see-the-chapter-change-explicitly-in-each-iteration-of-the-outer-loop-however-the-example-will-be-more-efficient-if-the-assignment-in-step-3-is-moved-before-the-first-line-in-step-2-so-that-the-assignment-is-performed-only-once-then-set-the-stayinsync-property-to-true-so-that-rsttitleauthor-will-implicitly-and-automatically-change-to-the-corresponding-chapter-whenever-rst-moves-to-a-new-row"></a><span data-ttu-id="b1553-113">(A propriedade [StayInSync](stayinsync-property-ado.md) é definida como FALSE para propósitos de ilustração  portanto, você pode consultar a alteração de capítulo explicitamente em cada iteração para o loop externo.</span><span class="sxs-lookup"><span data-stu-id="b1553-113">(The [StayInSync](stayinsync-property-ado.md) property is set to FALSE for purposes of illustration — so you can see the chapter change explicitly in each iteration of the outer loop.</span></span> <span data-ttu-id="b1553-114">No entanto, o exemplo será mais eficiente se a atribuição na etapa 3 for movida antes da primeira linha na etapa 2; de modo que a atribuição seja executada apenas uma vez.</span><span class="sxs-lookup"><span data-stu-id="b1553-114">However, the example will be more efficient if the assignment in step 3 is moved before the first line in step 2, so that the assignment is performed only once.</span></span> <span data-ttu-id="b1553-115">Em seguida, defina a propriedade **StayInSync** como TRUE, para que *rstTitleAuthor* automaticamente e implicitamente alterará o capítulo correspondente sempre que *rst* move para uma nova linha.)</span><span class="sxs-lookup"><span data-stu-id="b1553-115">Then set the **StayInSync** property to TRUE, so that *rstTitleAuthor* will implicitly and automatically change to the corresponding chapter whenever *rst* moves to a new row.)</span></span>
=======
1. <span data-ttu-id="b1553-116">Os objetos **Recordset** dos autores e as tabelas do autor de títulos são relacionados pelo ID do autor.</span><span class="sxs-lookup"><span data-stu-id="b1553-116">**Recordset** objects from the authors and titleauthor tables are related by author ID.</span></span>

2. <span data-ttu-id="b1553-117">O loop externo exibe o nome e sobrenome de cada autor, o estado e a identificação.</span><span class="sxs-lookup"><span data-stu-id="b1553-117">The outer loop displays each author's first and last name, state, and identification.</span></span>

3. <span data-ttu-id="b1553-118">O **Recordset** anexado para cada linha é recuperado da coleção **Fields** e designado ao *rstTitleAuthor*.</span><span class="sxs-lookup"><span data-stu-id="b1553-118">The appended **Recordset** for each row is retrieved from the **Fields** collection and assigned to *rstTitleAuthor*.</span></span>

4. <span data-ttu-id="b1553-119">O loop interno exibe quatro campos de cada linha no **Recordset** anexado.</span><span class="sxs-lookup"><span data-stu-id="b1553-119">The inner loop displays four fields from each row in the appended **Recordset**.</span></span>

> [!NOTE] 
> <span data-ttu-id="b1553-120">A propriedade [StayInSync](stayinsync-property-ado.md) é definida como FALSE para fins de ilustração, para que você possa ver o capítulo alterar explicitamente cada iteração do loop externo.</span><span class="sxs-lookup"><span data-stu-id="b1553-120">The [StayInSync](stayinsync-property-ado.md) property is set to FALSE for purposes of illustration, so you can see the chapter change explicitly in each iteration of the outer loop.</span></span> <span data-ttu-id="b1553-121">No entanto, o exemplo será mais eficiente se a atribuição na etapa 3 for movida antes da primeira linha na etapa 2; de modo que a atribuição seja executada apenas uma vez.</span><span class="sxs-lookup"><span data-stu-id="b1553-121">However, the example will be more efficient if the assignment in step 3 is moved before the first line in step 2, so that the assignment is performed only once.</span></span> <span data-ttu-id="b1553-122">Defina a propriedade **StayInSync** como TRUE, para que *rstTitleAuthor* automaticamente e implicitamente alterará o capítulo correspondente sempre que *rst* move para uma nova linha.</span><span class="sxs-lookup"><span data-stu-id="b1553-122">Set the **StayInSync** property to TRUE, so that *rstTitleAuthor* will implicitly and automatically change to the corresponding chapter whenever *rst* moves to a new row.</span></span>
>>>>>>> <span data-ttu-id="b1553-123">mestre</span><span class="sxs-lookup"><span data-stu-id="b1553-123">master</span></span>

<span data-ttu-id="b1553-124">**Exemplo**</span><span class="sxs-lookup"><span data-stu-id="b1553-124">**Example**</span></span>

```vb 
 
Sub datashape() 
 Dim cnn As New ADODB.Connection 
 Dim rst As New ADODB.Recordset 
 Dim rstTitleAuthor As New ADODB.Recordset 
 
 cnn.Provider = "MSDataShape" 
 cnn.Open "Data Provider=MSDASQL;" & _ 
 "Data Source=SRV;" & _ 
 "User Id=MyUserName;Password=MyPassword;Database=Pubs" 
' STEP 1 
 rst.StayInSync = FALSE 
 rst.Open "SHAPE {select * from authors} " & _ 
 "APPEND ({select * from titleauthor} " & _ 
 "RELATE au_id TO au_id) AS chapTitleAuthor", _ 
 cnn 
' STEP 2 
 While Not rst.EOF 
 Debug.Print rst("au_fname"), rst("au_lname"), _ 
 rst("state"), rst("au_id") 
' STEP 3 
 Set rstTitleAuthor = rst("chapTitleAuthor").Value 
' STEP 4 
 While Not rstTitleAuthor.EOF 
 Debug.Print rstTitleAuthor(0), rstTitleAuthor(1), _ 
 rstTitleAuthor(2), rstTitleAuthor(3) 
 rstTitleAuthor.MoveNext 
 Wend 
 rst.MoveNext 
 Wend 
End Sub 
```

