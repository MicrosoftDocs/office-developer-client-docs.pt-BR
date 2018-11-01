---
title: Propriedade Recordset.Filter (DAO)
TOCTitle: Filter Property
ms:assetid: feffa23b-c348-9718-ba4b-65db0f739789
ms:mtpsurl: https://msdn.microsoft.com/library/Ff837300(v=office.15)
ms:contentKeyID: 48548953
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 35ae33c9b7979e6dd98d94652a61c8737397c7a3
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25884300"
---
# <a name="recordsetfilter-property-dao"></a><span data-ttu-id="bbe31-102">Propriedade Recordset.Filter (DAO)</span><span class="sxs-lookup"><span data-stu-id="bbe31-102">Recordset.Filter Property (DAO)</span></span>

<span data-ttu-id="bbe31-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="bbe31-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="bbe31-p101">Define ou retornar um valor que determina os registros incluídos em um objeto **Recordset** aberto subsequentemente (somente espaços de trabalho do Microsoft Access). **String** de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="bbe31-p101">Sets or returns a value that determines the records included in a subsequently opened **Recordset** object (Microsoft Access workspaces only). Read/write **String**.</span></span>

## <a name="syntax"></a><span data-ttu-id="bbe31-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="bbe31-106">Syntax</span></span>

<span data-ttu-id="bbe31-107">*expressão* . Filtro</span><span class="sxs-lookup"><span data-stu-id="bbe31-107">*expression* .Filter</span></span>

<span data-ttu-id="bbe31-108">*expressão* Uma expressão que retorna um objeto **Recordset** .</span><span class="sxs-lookup"><span data-stu-id="bbe31-108">*expression* An expression that returns a **Recordset** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="bbe31-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="bbe31-109">Remarks</span></span>

<span data-ttu-id="bbe31-110">O valor de definição ou de retorno é um tipo de dados de cadeia de caracteres que contém a cláusula WHERE de uma instrução SQL sem a palavra reservada WHERE.</span><span class="sxs-lookup"><span data-stu-id="bbe31-110">The setting or return value is a String data type that contains the WHERE clause of an SQL statement without the reserved word WHERE.</span></span>

<span data-ttu-id="bbe31-111">Use a propriedade **Filter** para aplicar um filtro a um dynaset, instantâneo ou objeto **Recordset** do tipo somente encaminhamento.</span><span class="sxs-lookup"><span data-stu-id="bbe31-111">Use the **Filter** property to apply a filter to a dynaset–, snapshot–, or forward–only–type **Recordset** object.</span></span>

<span data-ttu-id="bbe31-112">Você pode usar a propriedade **Filter** para restringir os registros retornados de um objeto existente quando um novo objeto **Recordset** for aberto com base em um objeto **Recordset** existente.</span><span class="sxs-lookup"><span data-stu-id="bbe31-112">You can use the **Filter** property to restrict the records returned from an existing object when a new **Recordset** object is opened based on an existing **Recordset** object.</span></span>

<span data-ttu-id="bbe31-113">Utilize o formato de data dos EUA (mês-dia-ano) quando filtrar campos que contenham datas, mesmo se você não estiver usando a versão EUA do mecanismo de banco de dados do Microsoft Access (nesse caso, você deve montar quaisquer datas concatenando cadeias de caracteres, por exemplo, strMonth & "-" & strDay & "-" & strYear).</span><span class="sxs-lookup"><span data-stu-id="bbe31-113">Use the U.S. date format (month-day-year) when you filter fields containing dates, even if you're not using the U.S. version of the Microsoft Access database engine (in which case you must assemble any dates by concatenating strings, for example, strMonth & "-" & strDay & "-" & strYear).</span></span> <span data-ttu-id="bbe31-114">Caso contrário, é possível que os dados não sejam filtrados como esperado.</span><span class="sxs-lookup"><span data-stu-id="bbe31-114">Otherwise, the data may not be filtered as you expect.</span></span>

<span data-ttu-id="bbe31-115">Em vários casos, é mais rápido abrir um novo objeto **Recordset** usando uma instrução SQL que inclua uma cláusula WHERE.</span><span class="sxs-lookup"><span data-stu-id="bbe31-115">In many cases, it's faster to open a new **Recordset** object by using an SQL statement that includes a WHERE clause.</span></span>

<span data-ttu-id="bbe31-116">Se você definir a propriedade como uma cadeia de caracteres concatenada com um valor não – inteiro e os parâmetros do sistema especificarem um caractere decimal que fora dos EUA, como uma vírgula (por exemplo, strFilter = "preço \> " & lngPrice e lngPrice = 125,50), ocorrerá um erro ao tentar Abra o próximo **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="bbe31-116">If you set the property to a string concatenated with a non–integer value, and the system parameters specify a non-U.S. decimal character such as a comma (for example, strFilter = "PRICE \> " & lngPrice, and lngPrice = 125,50), an error occurs when you try to open the next **Recordset**.</span></span> <span data-ttu-id="bbe31-117">Isso acontecerá porque durante a concatenação, o número será convertido em uma sequência que usa o caractere decimal padrão do sistema e o Microsoft Access SQL aceita somente os caracteres decimais do padrão dos EUA.</span><span class="sxs-lookup"><span data-stu-id="bbe31-117">This is because during concatenation, the number will be converted to a string using your system's default decimal character, and Microsoft Access SQL only accepts U.S. decimal characters.</span></span>

## <a name="example"></a><span data-ttu-id="bbe31-118">Exemplo</span><span class="sxs-lookup"><span data-stu-id="bbe31-118">Example</span></span>

<span data-ttu-id="bbe31-119">O exemplo a seguir mostra como abrir uma propriedade Filter para determinar que registros incluir em um Recordset aberto subsequentemente.</span><span class="sxs-lookup"><span data-stu-id="bbe31-119">The following sample shows how to use the Filter property to determine the records to be included in a subsequently opened Recordset.</span></span>

<span data-ttu-id="bbe31-120">**Código de exemplo fornecido pela** [referência do programador do Microsoft Access 2010](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span><span class="sxs-lookup"><span data-stu-id="bbe31-120">**Sample code provided by** the [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span></span>

```vb
    Dim dbs As DAO.Database
    Dim rst As DAO.Recordset
    Dim rstFiltered As DAO.Recordset
    Dim strCity As String
    
    Set dbs = CurrentDb
    
    'Create the first filtered Recordset, returning customer records
    'for those visited between 30-60 days ago.
    Set rest = dbs.OpenRecordset(_ 
        "SELECT * FROM Customers WHERE LastVisitDate BETWEEN Date()-60 " & _
        "AND Date()-30 ORDER BY LastVisitDate DESC")
    
    'Begin row processing
    Do While Not rst.EOF
        
        'Retrieve the name of the first city in the selected rows
        strCity = rst!City
    
        'Now filter the Recordset to return only the customers from that city
        rst.Filter = "City = '" & strCity & "'"
        Set rstFiltered = rst.OpenRecordset
    
        'Process the rows
        Do While Not rstFiltered.EOF
            rstFiltered.Edit
            rstFiltered!ToBeVisited = True
            rstFiltered.Update
            rstFiltered.MoveNext
        Loop
    
        'We've done what was needed. Now exit
        Exit Do
        rst.MoveNext
       
    Loop
    
    'Cleanup
    rstFiltered.Close
    rst.Close
    
    Set rstFiltered = Nothing
    Set rst = Nothing
```
