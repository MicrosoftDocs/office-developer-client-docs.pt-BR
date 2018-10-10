---
title: Propriedade Recordset2.PercentPosition (DAO)
TOCTitle: PercentPosition Property
ms:assetid: 830a7d26-6817-233f-ce24-80b572c1c100
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196732(v=office.15)
ms:contentKeyID: 48545996
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052973
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 874f6a272dad72681e7f73ad3b1bafeecf6c688a
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25464744"
---
# <a name="recordset2percentposition-property-dao"></a><span data-ttu-id="6007e-102">Propriedade Recordset2.PercentPosition (DAO)</span><span class="sxs-lookup"><span data-stu-id="6007e-102">Recordset2.PercentPosition Property (DAO)</span></span>


<span data-ttu-id="6007e-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="6007e-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="6007e-104">Define ou retorna um valor que indica o local aproximado do registro atual no objeto **[Recordset](recordset-object-dao.md)** com base em uma porcentagem de registros no **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="6007e-104">Sets or returns a value indicating the approximate location of the current record in the **[Recordset](recordset-object-dao.md)** object based on a percentage of the records in the **Recordset**.</span></span>

## <a name="syntax"></a><span data-ttu-id="6007e-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6007e-105">Syntax</span></span>

<span data-ttu-id="6007e-106">*expressão* . PercentPosition</span><span class="sxs-lookup"><span data-stu-id="6007e-106">*expression* .PercentPosition</span></span>

<span data-ttu-id="6007e-107">*expressão* Uma variável que representa um objeto **Recordset2** .</span><span class="sxs-lookup"><span data-stu-id="6007e-107">*expression* A variable that represents a **Recordset2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="6007e-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="6007e-108">Remarks</span></span>

<span data-ttu-id="6007e-p101">Para indicar ou alterar a posição aproximada do registro atual em um objeto **Recordset**, você poderá verificar ou definir a propriedade **PercentPosition**. Quando você estiver trabalhando com um objeto **Recordset** do tipo dynaset ou instantâneo aberto diretamente a partir de uma tabela base, preencha primeiro o objeto **Recordset**, movendo-se para o último registro antes de definir ou verificar a propriedade **PercentPosition**. Se você usar a propriedade **PercentPosition** antes de preencher totalmente o objeto **Recordset**, a quantidade de movimento será relativa ao número de registros acessados, conforme indicado pela definição de propriedade **[RecordCount](recordset2-recordcount-property-dao.md)**. Você pode se mover para o último registro usando o método **[MoveLast](recordset2-movelast-method-dao.md)**.</span><span class="sxs-lookup"><span data-stu-id="6007e-p101">To indicate or change the approximate position of the current record in a **Recordset** object, you can check or set the **PercentPosition** property. When working with a dynaset- or snapshot-type **Recordset** object opened directly from a base table, first populate the **Recordset** object by moving to the last record before you set or check the **PercentPosition** property. If you use the **PercentPosition** property before fully populating the **Recordset** object, the amount of movement is relative to the number of records accessed as indicated by the **[RecordCount](recordset2-recordcount-property-dao.md)** property setting. You can move to the last record by using the **[MoveLast](recordset2-movelast-method-dao.md)** method.</span></span>


> [!NOTE]
> <P><span data-ttu-id="6007e-113">[!OBSERVAçãO] O uso da propriedade <STRONG>PercentPosition</STRONG> para mover o registro atual para um registro específico em um objeto <STRONG>Recordset</STRONG> não é recomendável? A propriedade <STRONG><A href="recordset2-bookmark-property-dao.md">Bookmark</A></STRONG> é a mais adequada para essa tarefa.</span><span class="sxs-lookup"><span data-stu-id="6007e-113">Using the <STRONG>PercentPosition</STRONG> property to move the current record to a specific record in a <STRONG>Recordset</STRONG> object isn't recommended?the <STRONG><A href="recordset2-bookmark-property-dao.md">Bookmark</A></STRONG> property is better suited for this task.</span></span></P>



<span data-ttu-id="6007e-p102">Assim que você definir a propriedade **PercentPosition** para um valor, o registro na posição aproximada que corresponder a esse valor se tornará o valor atual e a propriedade **PercentPosition** será redefinida para um valor que refletir a posição aproximada do registro atual. Por exemplo, se o objeto **Recordset** contiver somente cinco registros e você definir o valor da propriedade **PercentPosition** como 77, o valor retornado da propriedade **PercentPosition** poderá ser 80 e não 77.</span><span class="sxs-lookup"><span data-stu-id="6007e-p102">Once you set the **PercentPosition** property to a value, the record at the approximate position corresponding to that value becomes current, and the **PercentPosition** property is reset to a value that reflects the approximate position of the current record. For example, if your **Recordset** object contains only five records, and you set its **PercentPosition** property value to 77, the value returned from the **PercentPosition** property may be 80, not 77.</span></span>

<span data-ttu-id="6007e-116">A propriedade **PercentPosition** se aplica a todos os tipos de objetos **Recordset** , exceto os objetos **Recordset** tipo somente encaminhamento ou objetos **Recordset** abertos a partir de consultas passagem nos bancos de dados remotos.</span><span class="sxs-lookup"><span data-stu-id="6007e-116">The **PercentPosition** property applies to all types of **Recordset** objects except for forward–only–type **Recordset** objects or **Recordset** objects opened from pass-through queries against remote databases.</span></span>

<span data-ttu-id="6007e-117">Use a propriedade **PercentPosition** com uma barra de rolagem em um formulário ou uma caixa de texto para indicar o local do registro atual em um objeto **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="6007e-117">You can use the **PercentPosition** property with a scroll bar on a form or text box to indicate the location of the current record in a **Recordset** object.</span></span>

## <a name="example"></a><span data-ttu-id="6007e-118">Exemplo</span><span class="sxs-lookup"><span data-stu-id="6007e-118">Example</span></span>

<span data-ttu-id="6007e-119">Este exemplo usa a propriedade **PercentPosition** para mostrar a posição do ponteiro do registro atual relativa ao início do **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="6007e-119">This example uses the **PercentPosition** property to show the position of the current record pointer relative to the beginning of the **Recordset**.</span></span>

```vb
    Sub PercentPositionX() 
     
     Dim dbsNorthwind As Database 
     Dim rstProducts As Recordset2 
     Dim strFind As String 
     Dim strMessage As String 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     ' PercentPosition only works with dynasets or snapshots. 
     Set rstProducts = dbsNorthwind.OpenRecordset( _ 
     "SELECT ProductName FROM Products " & _ 
     "ORDER BY ProductName", dbOpenSnapshot) 
     
     With rstProducts 
     ' Populate the Recordset. 
     .MoveLast 
     .MoveFirst 
     
     Do While True 
     ' Show current record information and ask user 
     ' for input. 
     strMessage = "Product: " & !ProductName & vbCr & _ 
     "The record pointer is " & _ 
     Format(.PercentPosition, "##0.0") & _ 
     "% from the " & vbCr & _ 
     "beginning of the Recordset." & vbCr & _ 
     "Please enter a character search string " & _ 
     "for a product name." 
     strFind = Trim(InputBox(strMessage)) 
     If strFind = "" Then Exit Do 
     
     ' Try to find a record matching the search string. 
     .FindFirst "ProductName >= '" & strFind & "'" 
     If .NoMatch Then .MoveLast 
     Loop 
     
     .Close 
     End With 
     
     dbsNorthwind.Close 
     
    End Sub
```
