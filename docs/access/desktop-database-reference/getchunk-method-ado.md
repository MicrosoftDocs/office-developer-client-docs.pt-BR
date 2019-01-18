---
title: Método GetChunk (ADO)
TOCTitle: GetChunk method (ADO)
ms:assetid: 1ef1c37a-8453-8d3b-251a-d16e0d519fd7
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248979(v=office.15)
ms:contentKeyID: 48543629
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 44cd0cb5632e64811de14f9abd3c78aac9203705
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28698180"
---
# <a name="getchunk-method-ado"></a><span data-ttu-id="fa4e0-102">Método GetChunk (ADO)</span><span class="sxs-lookup"><span data-stu-id="fa4e0-102">GetChunk method (ADO)</span></span>

<span data-ttu-id="fa4e0-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="fa4e0-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="fa4e0-104">Retorna todo, ou uma porção de, o conteúdo de um grande objeto [Field](field-object-ado.md) de dados binários ou texto.</span><span class="sxs-lookup"><span data-stu-id="fa4e0-104">Returns all, or a portion, of the contents of a large text or binary data [Field](field-object-ado.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="fa4e0-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="fa4e0-105">Syntax</span></span>

<span data-ttu-id="fa4e0-106">*variável* = *campo*. GetChunk (*tamanho* )</span><span class="sxs-lookup"><span data-stu-id="fa4e0-106">*variable* = *field*.GetChunk(*Size* )</span></span>

## <a name="return-value"></a><span data-ttu-id="fa4e0-107">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="fa4e0-107">Return value</span></span>

<span data-ttu-id="fa4e0-108">Retorna uma **Variant**.</span><span class="sxs-lookup"><span data-stu-id="fa4e0-108">Returns a **Variant**.</span></span>

## <a name="parameters"></a><span data-ttu-id="fa4e0-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="fa4e0-109">Parameters</span></span>

|<span data-ttu-id="fa4e0-110">Parâmetro</span><span class="sxs-lookup"><span data-stu-id="fa4e0-110">Parameter</span></span>|<span data-ttu-id="fa4e0-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="fa4e0-111">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="fa4e0-112">*Tamanho*</span><span class="sxs-lookup"><span data-stu-id="fa4e0-112">*Size*</span></span> |<span data-ttu-id="fa4e0-113">Uma expressão **Long** que é igual ao número de bytes ou caracteres que você deseja recuperar.</span><span class="sxs-lookup"><span data-stu-id="fa4e0-113">A **Long** expression that is equal to the number of bytes or characters that you want to retrieve.</span></span>|

## <a name="remarks"></a><span data-ttu-id="fa4e0-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="fa4e0-114">Remarks</span></span>

<span data-ttu-id="fa4e0-p101">Utilize o método **GetChunk** em um objeto **Field** para recuperar parte ou todos os seus dados de caracteres ou binários longos. Em situações em que a memória do sistema seja limitada, é possível utilizar o método **GetChunk** para manipular valores longos em porções, em vez de em sua totalidade.</span><span class="sxs-lookup"><span data-stu-id="fa4e0-p101">Use the **GetChunk** method on a **Field** object to retrieve part or all of its long binary or character data. In situations where system memory is limited, you can use the **GetChunk** method to manipulate long values in portions, rather than in their entirety.</span></span>

<span data-ttu-id="fa4e0-p102">Os dados retornados por **GetChunk** são atribuídos a *variable*. Se *Size* for maior que os dados restantes, o método **GetChunk** retornará somente esses dados sem preencher *variable* com espaços vazios. Se o campo estiver vazio, o método **GetChunk** retornará um valor nulo.</span><span class="sxs-lookup"><span data-stu-id="fa4e0-p102">The data that a **GetChunk** call returns is assigned to *variable*. If *Size* is greater than the remaining data, the **GetChunk** method returns only the remaining data without padding *variable* with empty spaces. If the field is empty, the **GetChunk** method returns a null value.</span></span>

<span data-ttu-id="fa4e0-p103">Cada chamada subsequente a **GetChunk** recupera os dados a partir de onde a chamada anterior a **GetChunk** foi suspensa. No entanto, se estiver recuperando dados a partir de um campo e, em seguida, definir ou ler o valor de outro campo no registro atual, o ADO supõe que você concluiu a recuperação de dados do primeiro campo. Se você chamar o método **GetChunk** no primeiro campo novamente, o ADO interpreta a chamada como uma nova operação **GetChunk** e começara a ler a partir do início dos dados. O acesso a campos em outros objetos [Recordset](recordset-object-ado.md) que não sejam clones do primeiro objeto **Recordset** não interromperão as operações **GetChunk**.</span><span class="sxs-lookup"><span data-stu-id="fa4e0-p103">Each subsequent **GetChunk** call retrieves data starting from where the previous **GetChunk** call left off. However, if you are retrieving data from one field and then you set or read the value of another field in the current record, ADO assumes you have finished retrieving data from the first field. If you call the **GetChunk** method on the first field again, ADO interprets the call as a new **GetChunk** operation and starts reading from the beginning of the data. Accessing fields in other [Recordset](recordset-object-ado.md) objects that are not clones of the first **Recordset** object will not disrupt **GetChunk** operations.</span></span>

<span data-ttu-id="fa4e0-124">Se o bit **adFldLong** na propriedade [Attributes](attributes-property-ado.md) de um objeto **Field** for definido como **True**, será possível utilizar o método **GetChunk** para esse campo.</span><span class="sxs-lookup"><span data-stu-id="fa4e0-124">If the **adFldLong** bit in the [Attributes](attributes-property-ado.md) property of a **Field** object is set to **True**, you can use the **GetChunk** method for that field.</span></span>

<span data-ttu-id="fa4e0-125">Se não houver um registro atual ao utilizar o método **GetChunk** em um objeto **Field**, ocorrerá o erro 3021 (sem registro atual).</span><span class="sxs-lookup"><span data-stu-id="fa4e0-125">If there is no current record when you use the **GetChunk** method on a **Field** object, error 3021 (no current record) occurs.</span></span>


> [!NOTE]
> <span data-ttu-id="fa4e0-p104">[!OBSERVAçãO] O método **GetChunk** não opera em objetos **Field** de um objeto [Record](record-object-ado.md). Ele não executa nenhuma operação e produzirá um erro em tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="fa4e0-p104">The **GetChunk** method does not operate on **Field** objects of a [Record](record-object-ado.md) object. It does not perform any operation and will produce a run-time error.</span></span>


