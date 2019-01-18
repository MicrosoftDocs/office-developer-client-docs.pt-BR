---
title: Método AppendChunk (ADO)
TOCTitle: AppendChunk method (ADO)
ms:assetid: 3fa931a3-2cd7-a3b0-a750-40e18bc9937e
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249179(v=office.15)
ms:contentKeyID: 48544405
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 89a75ebe8a3fe704c4f755a0f744eac4d068ec0a
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28702926"
---
# <a name="appendchunk-method-ado"></a><span data-ttu-id="46b11-102">Método AppendChunk (ADO)</span><span class="sxs-lookup"><span data-stu-id="46b11-102">AppendChunk method (ADO)</span></span>

<span data-ttu-id="46b11-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="46b11-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="46b11-104">Acrescenta dados a um objeto [Field](field-object-ado.md) ou [Parameter](parameter-object-ado.md) de dados binários ou de texto longos.</span><span class="sxs-lookup"><span data-stu-id="46b11-104">Appends data to a large text or binary data [Field](field-object-ado.md), or to a [Parameter](parameter-object-ado.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="46b11-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="46b11-105">Syntax</span></span>

<span data-ttu-id="46b11-106">*objeto.* AppendChunk *dados*</span><span class="sxs-lookup"><span data-stu-id="46b11-106">*object.* AppendChunk *Data*</span></span>

## <a name="parameters"></a><span data-ttu-id="46b11-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="46b11-107">Parameters</span></span>

|<span data-ttu-id="46b11-108">Parâmetro</span><span class="sxs-lookup"><span data-stu-id="46b11-108">Parameter</span></span>|<span data-ttu-id="46b11-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="46b11-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="46b11-110">*objeto*</span><span class="sxs-lookup"><span data-stu-id="46b11-110">*object*</span></span> |<span data-ttu-id="46b11-111">Um objeto **Field** ou **Parameter**.</span><span class="sxs-lookup"><span data-stu-id="46b11-111">A **Field** or **Parameter** object.</span></span>|
|<span data-ttu-id="46b11-112">*Data*</span><span class="sxs-lookup"><span data-stu-id="46b11-112">*Data*</span></span> |<span data-ttu-id="46b11-113">Um **Variant** que contém os dados a serem acrescentados ao objeto.</span><span class="sxs-lookup"><span data-stu-id="46b11-113">A **Variant** that contains the data to append to the object.</span></span>|

## <a name="remarks"></a><span data-ttu-id="46b11-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="46b11-114">Remarks</span></span>

<span data-ttu-id="46b11-115">Use o método **AppendChunk** em um objeto **Field** ou **Parameter** preenchê-lo com dados binários longos ou caracteres.</span><span class="sxs-lookup"><span data-stu-id="46b11-115">Use the **AppendChunk** method on a **Field** or **Parameter** object to fill it with long binary or character data.</span></span> <span data-ttu-id="46b11-116">Em situações em que a memória do sistema é limitada, você pode usar o método **AppendChunk** para manipular valores longos em partes, e não em sua totalidade.</span><span class="sxs-lookup"><span data-stu-id="46b11-116">In situations where system memory is limited, you can use the **AppendChunk** method to manipulate long values in portions rather than in their entirety.</span></span>

### <a name="field"></a><span data-ttu-id="46b11-117">Campo</span><span class="sxs-lookup"><span data-stu-id="46b11-117">Field</span></span>

<span data-ttu-id="46b11-118">Se o bit **adFldLong** na propriedade [Attributes](attributes-property-ado.md) de um objeto **Field** for definido como true, você poderá usar o método **AppendChunk** para esse campo.</span><span class="sxs-lookup"><span data-stu-id="46b11-118">If the **adFldLong** bit in the [Attributes](attributes-property-ado.md) property of a **Field** object is set to true, you can use the **AppendChunk** method for that field.</span></span>

<span data-ttu-id="46b11-p102">A primeira chamada de **AppendChunk** em um objeto **Field** grava dados no campo, substituindo os dados existentes. As chamadas subsequentes de **AppendChunk** são adicionadas aos dados existentes. Se você estiver acrescentando dados a um campo e, em seguida, definir ou ler o valor de outro campo no registro atual, o ADO assumirá que você concluiu o acréscimo de dados ao primeiro campo. Se você chamar o método **AppendChunk** novamente no primeiro campo, o ADO interpretará a chamada como uma nova operação **AppendChunk** e substituirá os dados existentes. O acesso a campos em outros objetos [Recordset](recordset-object-ado.md) que não sejam clones do primeiro objeto **Recordset** não interromperá as operações de **AppendChunk**.</span><span class="sxs-lookup"><span data-stu-id="46b11-p102">The first **AppendChunk** call on a **Field** object writes data to the field, overwriting any existing data. Subsequent **AppendChunk** calls add to existing data. If you are appending data to one field and then you set or read the value of another field in the current record, ADO assumes that you are finished appending data to the first field. If you call the **AppendChunk** method on the first field again, ADO interprets the call as a new **AppendChunk** operation and overwrites the existing data. Accessing fields in other [Recordset](recordset-object-ado.md) objects that are not clones of the first **Recordset** object will not disrupt **AppendChunk** operations.</span></span>

<span data-ttu-id="46b11-124">Um erro ocorrerá se não houver registro atual quando você chamar **AppendChunk** em um objeto **Field**.</span><span class="sxs-lookup"><span data-stu-id="46b11-124">If there is no current record when you call **AppendChunk** on a **Field** object, an error occurs.</span></span>

> [!NOTE]
> <span data-ttu-id="46b11-p103">[!OBSERVAçãO] O método **AppendChunk** não é operado nos objeto **Field** de um objeto [Record](record-object-ado.md). Ele não executa nenhuma operação e produzirá um erro em tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="46b11-p103">The **AppendChunk** method does not operate on **Field** objects of a [Record](record-object-ado.md) object. It does not perform any operation and will produce a run-time error.</span></span>

### <a name="parameters"></a><span data-ttu-id="46b11-127">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="46b11-127">Parameters</span></span>

<span data-ttu-id="46b11-128">Se o bit **adParamLong** na propriedade **Attributes** de um objeto **Parameter** for definido como true, você poderá usar o método **AppendChunk** para esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="46b11-128">If the **adParamLong** bit in the **Attributes** property of a **Parameter** object is set to true, you can use the **AppendChunk** method for that parameter.</span></span>

<span data-ttu-id="46b11-p104">A primeira chamada de **AppendChunk** em um objeto **Parameter** grava dados no parâmetro, substituindo os dados existentes. As chamadas subsequentes de **AppendChunk** em um objeto **Parameter** são adicionadas aos dados de parâmetro existentes. A chamada de **AppendChunk** que passar um valor nulo descartará todos os dados de parâmetro.</span><span class="sxs-lookup"><span data-stu-id="46b11-p104">The first **AppendChunk** call on a **Parameter** object writes data to the parameter, overwriting any existing data. Subsequent **AppendChunk** calls on a **Parameter** object add to existing parameter data. An **AppendChunk** call that passes a null value discards all of the parameter data.</span></span>

