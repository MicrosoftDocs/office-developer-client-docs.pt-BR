---
title: Propriedade Recordset.Filter (DAO)
TOCTitle: Filter Property
ms:assetid: feffa23b-c348-9718-ba4b-65db0f739789
ms:mtpsurl: https://msdn.microsoft.com/library/Ff837300(v=office.15)
ms:contentKeyID: 48548953
ms.date: 06/04/2019
mtps_version: v=office.15
localization_priority: Priority
ms.openlocfilehash: 43afbfda8c560eafb90e6a53d85207e19e5b1170
ms.sourcegitcommit: 4a570873914c58dd4cdbe97b5d9ec41866dc797c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/03/2019
ms.locfileid: "34675747"
---
# <a name="recordsetfilter-property-dao"></a><span data-ttu-id="2654c-102">Propriedade Recordset.Filter (DAO)</span><span class="sxs-lookup"><span data-stu-id="2654c-102">Recordset.Filter property (DAO)</span></span>

<span data-ttu-id="2654c-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="2654c-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="2654c-104">Define ou retorna um valor que determina os registros incluídos em um objeto **Recordset** aberto posteriormente (somente nos espaços de trabalho do Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="2654c-104">Sets or returns a value that determines the records included in a subsequently opened **Recordset** object (Microsoft Access workspaces only).</span></span> <span data-ttu-id="2654c-105">**String** de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="2654c-105">Read/write **String**.</span></span>

## <a name="syntax"></a><span data-ttu-id="2654c-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2654c-106">Syntax</span></span>

<span data-ttu-id="2654c-107">*expressão*.**Filtro**</span><span class="sxs-lookup"><span data-stu-id="2654c-107">expression .Filter</span></span>

<span data-ttu-id="2654c-108">*expressão* Uma expressão que retorna um objeto **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="2654c-108">*expression* An expression that returns a **Recordset** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="2654c-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="2654c-109">Remarks</span></span>

<span data-ttu-id="2654c-110">O valor de definição ou de retorno é um tipo de dados de cadeia de caracteres que contém a cláusula WHERE de uma instrução SQL sem a palavra reservada WHERE.</span><span class="sxs-lookup"><span data-stu-id="2654c-110">The setting or return value is a String data type that contains the WHERE clause of an SQL statement without the reserved word WHERE.</span></span>

<span data-ttu-id="2654c-111">Use a propriedade **Filter** para aplicar um filtro a um objeto **Recordset** do tipo dynaset, instantâneo ou somente encaminhamento.</span><span class="sxs-lookup"><span data-stu-id="2654c-111">Use the **Filter** property to apply a filter to a dynaset–, snapshot–, or forward–only–type **Recordset** object.</span></span>

<span data-ttu-id="2654c-112">Você pode usar a propriedade **Filter** para restringir os registros retornados de um objeto existente quando um novo objeto **Recordset** for aberto com base em um objeto **Recordset** existente.</span><span class="sxs-lookup"><span data-stu-id="2654c-112">You can use the **Filter** property to restrict the records returned from an existing object when a new **Recordset** object is opened based on an existing **Recordset** object.</span></span>

<span data-ttu-id="2654c-113">Use o formato de dados dos EUA (mês-dia-ano) quando você filtra campos com datas, mesmo se você não estiver usando a versão dos EUA do mecanismo de banco de dados do Microsoft Access (nesse caso, você deverá montar todas as datas ao concatenar cadeias de caracteres, por exemplo, strMonth & "-" & strDay & "-" & strYear).</span><span class="sxs-lookup"><span data-stu-id="2654c-113">Use the U.S. date format (month-day-year) when you filter fields containing dates, even if you're not using the U.S. version of the Microsoft Access database engine (in which case you must assemble any dates by concatenating strings, for example, strMonth & "-" & strDay & "-" & strYear).</span></span> <span data-ttu-id="2654c-114">Caso contrário, é possível que os dados não sejam filtrados como esperado.</span><span class="sxs-lookup"><span data-stu-id="2654c-114">Otherwise, the data may not be filtered as you expect.</span></span>

<span data-ttu-id="2654c-115">Em vários casos, é mais rápido abrir um novo objeto **Recordset** usando uma instrução SQL que inclua uma cláusula WHERE.</span><span class="sxs-lookup"><span data-stu-id="2654c-115">In many cases, it's faster to open a new **Recordset** object by using an SQL statement that includes a WHERE clause.</span></span>

<span data-ttu-id="2654c-116">Se você definir a propriedade como uma cadeia de caracteres concatenada com um valor não inteiro, e se os parâmetros do sistema especificarem um caractere decimal não americano, como uma vírgula (por exemplo, strFilter = "PRICE > \>" & lngPrice e lngPrice = 125,50), ocorrerá um erro quando você tentar abrir o próximo **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="2654c-116">If you set the property to a string concatenated with a non–integer value, and the system parameters specify a non-U.S. decimal character such as a comma (for example, strFilter = "PRICE \> " & lngPrice, and lngPrice = 125,50), an error occurs when you try to open the next **Recordset**.</span></span> <span data-ttu-id="2654c-117">Isso acontecerá porque durante a concatenação, o número será convertido em uma sequência que usa o caractere decimal padrão do sistema e o Microsoft Access SQL aceita somente os caracteres decimais do padrão dos EUA.</span><span class="sxs-lookup"><span data-stu-id="2654c-117">This is because during concatenation, the number will be converted to a string using your system's default decimal character, and Microsoft Access SQL only accepts U.S. decimal characters.</span></span>

## <a name="example"></a><span data-ttu-id="2654c-118">Exemplo</span><span class="sxs-lookup"><span data-stu-id="2654c-118">Example</span></span>

<span data-ttu-id="2654c-119">O exemplo a seguir mostra como usar a propriedade Filter para determinar que registros incluir em um Recordset aberto subsequentemente.</span><span class="sxs-lookup"><span data-stu-id="2654c-119">The following sample shows how to use the Filter property to determine the records to be included in a subsequently opened Recordset.</span></span>

<span data-ttu-id="2654c-120">**Código de exemplo fornecido por:** a [Referência do programador do Microsoft Access 2010](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span><span class="sxs-lookup"><span data-stu-id="2654c-120">**Sample code provided by** the [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span></span>

```vb
    Dim dbs As DAO.Database
    Dim rst As DAO.Recordset
    Dim rstFiltered As DAO.Recordset
    Dim strCity As String
    
    Set dbs = CurrentDb
    
    'Create the first filtered Recordset, returning customer records
    'for those visited between 30-60 days ago.
    Set rst = dbs.OpenRecordset(_ 
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
