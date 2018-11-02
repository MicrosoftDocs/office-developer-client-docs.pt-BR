---
title: Objeto Error - ActiveX Data Objects (ADO)
TOCTitle: Error object (ADO)
ms:assetid: 97e478bf-8b25-03a8-9358-abba5069cba3
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249678(v=office.15)
ms:contentKeyID: 48546477
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: f6a18570071428bfbd92d6674ca281234ea883bf
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25925209"
---
# <a name="error-object-ado"></a><span data-ttu-id="13e39-102">Objeto Error (ADO)</span><span class="sxs-lookup"><span data-stu-id="13e39-102">Error object (ADO)</span></span>


<span data-ttu-id="13e39-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="13e39-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="13e39-104">Contém os detalhes sobre os erros de acesso aos dados que pertencem à uma única operação que envolve o provedor.</span><span class="sxs-lookup"><span data-stu-id="13e39-104">Contains details about data access errors that pertain to a single operation involving the provider.</span></span>

## <a name="remarks"></a><span data-ttu-id="13e39-105">Comentários</span><span class="sxs-lookup"><span data-stu-id="13e39-105">Remarks</span></span>

<span data-ttu-id="13e39-p101">Qualquer operação envolvendo os objetos ADO pode gerar um ou vários erros de provedor. À medida que cada erro ocorrer, um ou vários objetos **Error** serão colocados na coleção [Errors](errors-collection-ado.md) do objeto [Connection](connection-object-ado.md). Quando a operação do ADO gerar um erro, a coleção **Errors** será limpa e o novo conjunto de objetos **Error** será colocado na coleção **Errors**.</span><span class="sxs-lookup"><span data-stu-id="13e39-p101">Any operation involving ADO objects can generate one or more provider errors. As each error occurs, one or more **Error** objects are placed in the [Errors](errors-collection-ado.md) collection of the [Connection](connection-object-ado.md) object. When another ADO operation generates an error, the **Errors** collection is cleared, and the new set of **Error** objects is placed in the **Errors** collection.</span></span>

> [!NOTE]
> <span data-ttu-id="13e39-p102">[!OBSERVAçãO] Cada objeto **Error** representa um erro de provedor específico e não um erro do ADO. Os erros do ADO são apresentados no mecanismo de tratamento de exceções do tempo de execução. Por exemplo, no Microsoft Visual Basic, a ocorrência de um erro específico de ADO disparará um evento **On Error** e aparecerá no objeto **Error**. Para obter uma lista completa dos erros do ADO, consulte o tópico [ErrorValueEnum](errorvalueenum.md).</span><span class="sxs-lookup"><span data-stu-id="13e39-p102">Each **Error** object represents a specific provider error, not an ADO error. ADO errors are exposed to the run-time exception-handling mechanism. For example, in Microsoft Visual Basic, the occurrence of an ADO-specific error will trigger an **On Error** event and appear in the **Error** object. For a complete list of ADO errors, see the [ErrorValueEnum](errorvalueenum.md) topic.</span></span>

<span data-ttu-id="13e39-113">Leia as propriedades do objeto **Error** para obter os detalhes específicos sobre cada erro, incluindo o seguinte:</span><span class="sxs-lookup"><span data-stu-id="13e39-113">You can read an **Error** object's properties to obtain specific details about each error, including the following:</span></span>

- <span data-ttu-id="13e39-p103">A propriedade [Description](description-property-ado.md), que contém o texto do erro. Esta é a propriedade padrão.</span><span class="sxs-lookup"><span data-stu-id="13e39-p103">The [Description](description-property-ado.md) property, which contains the text of the error. This is the default property.</span></span>

- <span data-ttu-id="13e39-116">A propriedade [Number](number-property-ado.md), que contém o valor inteiro **Long** da constante de erro.</span><span class="sxs-lookup"><span data-stu-id="13e39-116">The [Number](number-property-ado.md) property, which contains the **Long** integer value of the error constant.</span></span>

- <span data-ttu-id="13e39-p104">A propriedade [Source](source-property-ado-error.md), que identifica o objeto que causou o erro. Isso será particularmente útil quando você tiver vários objetos **Error** na coleção **Errors** depois de uma solicitação de uma fonte de dados.</span><span class="sxs-lookup"><span data-stu-id="13e39-p104">The [Source](source-property-ado-error.md) property, which identifies the object that raised the error. This is particularly useful when you have several **Error** objects in the **Errors** collection following a request to a data source.</span></span>

- <span data-ttu-id="13e39-119">As propriedades [SQLState](sqlstate-property-ado.md) e [NativeError](nativeerror-property-ado.md) que fornecem informações a partir das fontes de dados SQL.</span><span class="sxs-lookup"><span data-stu-id="13e39-119">The [SQLState](sqlstate-property-ado.md) and [NativeError](nativeerror-property-ado.md) properties, which provide information from SQL data sources.</span></span>

<span data-ttu-id="13e39-p105">Quando ocorrer um erro de provedor, este será colocado na coleção **Errors** do objeto **Connection**. O ADO suporta o retorno de vários erros ocasionados uma única operação do ADO para levar em conta as informações específicas do erro para o provedor. Para obter essas valiosas informações do erro em um manipulador de erros, use os recursos adequados para a interceptação de erros do idioma ou do ambiente no qual você estiver trabalhando e depois use os loops aninhados para enumerar as propriedades de cada objeto **Error** na coleção **Errors**.</span><span class="sxs-lookup"><span data-stu-id="13e39-p105">When a provider error occurs, it is placed in the **Errors** collection of the **Connection** object. ADO supports the return of multiple errors by a single ADO operation to allow for error information specific to the provider. To obtain this rich error information in an error handler, use the appropriate error-trapping features of the language or environment you are working with, then use nested loops to enumerate the properties of each **Error** object in the **Errors** collection.</span></span>

<span data-ttu-id="13e39-123">**Microsoft Visual Basic e usuários do VBScript** Se não houver nenhum objeto de **Conexão** válido, você precisará recuperar informações de erro do objeto **Error** .</span><span class="sxs-lookup"><span data-stu-id="13e39-123">**Microsoft Visual Basic and VBScript Users**If there is no valid **Connection** object, you will need to retrieve error information from the **Error** object.</span></span>

<span data-ttu-id="13e39-p106">Exatamente como os provedores fazem, o ADO limpa o objeto **OLE Error Info** antes de fazer uma chamada que poderia gerar potencialmente um novo erro de provedor. No entanto, a coleção **Errors** no objeto **Connection** será limpa e preenchida somente quando o provedor gerar um novo erro ou quando o método [Clear](clear-method-ado.md) for chamado.</span><span class="sxs-lookup"><span data-stu-id="13e39-p106">Just as providers do, ADO clears the **OLE Error Info** object before making a call that could potentially generate a new provider error. However, the **Errors** collection on the **Connection** object is cleared and populated only when the provider generates a new error, or when the [Clear](clear-method-ado.md) method is called.</span></span>

<span data-ttu-id="13e39-p107">Algumas propriedades e métodos retornam avisos que aparecem como objetos **Error** na coleção **Errors** mas não suspendem a execução de um programa. Antes de chamar os métodos [Resync](resync-method-ado.md), [UpdateBatch](updatebatch-method-ado.md) ou [CancelBatch](cancelbatch-method-ado.md) em um objeto [Recordset](recordset-object-ado.md), o método [Open](open-method-ado-connection.md) em um objeto **Connection** ou definir a propriedade [Filter](filter-property-ado.md) em um objeto **Recordset**, chame o método **Clear** na coleção **Errors**. Dessa forma, será possível ler a propriedade [Count](count-property-ado.md) da coleção **Errors** para verificar os avisos retornados.</span><span class="sxs-lookup"><span data-stu-id="13e39-p107">Some properties and methods return warnings that appear as **Error** objects in the **Errors** collection but do not halt a program's execution. Before you call the [Resync](resync-method-ado.md), [UpdateBatch](updatebatch-method-ado.md), or [CancelBatch](cancelbatch-method-ado.md) methods on a [Recordset](recordset-object-ado.md) object; the [Open](open-method-ado-connection.md) method on a **Connection** object; or set the [Filter](filter-property-ado.md) property on a **Recordset** object, call the **Clear** method on the **Errors** collection. That way, you can read the [Count](count-property-ado.md) property of the **Errors** collection to test for returned warnings.</span></span>

