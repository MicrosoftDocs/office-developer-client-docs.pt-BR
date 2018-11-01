---
title: Método AppendChunk (ADO)
TOCTitle: AppendChunk Method (ADO)
ms:assetid: 3fa931a3-2cd7-a3b0-a750-40e18bc9937e
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249179(v=office.15)
ms:contentKeyID: 48544405
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 3e13ebd5d222bc765fe2e38198588274508baa4a
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25881934"
---
# <a name="appendchunk-method-ado"></a><span data-ttu-id="c2f34-102">Método AppendChunk (ADO)</span><span class="sxs-lookup"><span data-stu-id="c2f34-102">AppendChunk Method (ADO)</span></span>


<span data-ttu-id="c2f34-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="c2f34-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="c2f34-104">Acrescenta dados a um objeto [Field](field-object-ado.md) ou [Parameter](parameter-object-ado.md) de dados binários ou de texto longos.</span><span class="sxs-lookup"><span data-stu-id="c2f34-104">Appends data to a large text or binary data [Field](field-object-ado.md), or to a [Parameter](parameter-object-ado.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="c2f34-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c2f34-105">Syntax</span></span>

<span data-ttu-id="c2f34-106">*objeto.* AppendChunk *dados*</span><span class="sxs-lookup"><span data-stu-id="c2f34-106">*object.* AppendChunk *Data*</span></span>

## <a name="parameters"></a><span data-ttu-id="c2f34-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c2f34-107">Parameters</span></span>

  - <span data-ttu-id="c2f34-108">*object*</span><span class="sxs-lookup"><span data-stu-id="c2f34-108">*object*</span></span>

  - <span data-ttu-id="c2f34-109">Um objeto **Field** ou **Parameter**.</span><span class="sxs-lookup"><span data-stu-id="c2f34-109">A **Field** or **Parameter** object.</span></span>

  - <span data-ttu-id="c2f34-110">*Data*</span><span class="sxs-lookup"><span data-stu-id="c2f34-110">*Data*</span></span>

  - <span data-ttu-id="c2f34-111">Um **Variant** que contém os dados a serem acrescentados ao objeto.</span><span class="sxs-lookup"><span data-stu-id="c2f34-111">A **Variant** that contains the data to append to the object.</span></span>

## <a name="remarks"></a><span data-ttu-id="c2f34-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="c2f34-112">Remarks</span></span>

<span data-ttu-id="c2f34-113">Use o método **AppendChunk** em um objeto **Field** ou **Parameter** preenchê-lo com dados binários longos ou caracteres.</span><span class="sxs-lookup"><span data-stu-id="c2f34-113">Use the **AppendChunk** method on a **Field** or **Parameter** object to fill it with long binary or character data.</span></span> <span data-ttu-id="c2f34-114">Em situações em que a memória do sistema é limitada, você pode usar o método **AppendChunk** para manipular valores longos em partes, e não em sua totalidade.</span><span class="sxs-lookup"><span data-stu-id="c2f34-114">In situations where system memory is limited, you can use the **AppendChunk** method to manipulate long values in portions rather than in their entirety.</span></span>

<span data-ttu-id="c2f34-115">**Objeto Field**</span><span class="sxs-lookup"><span data-stu-id="c2f34-115">**Field**</span></span>

<span data-ttu-id="c2f34-116">Se o bit **adFldLong** na propriedade [Attributes](attributes-property-ado.md) de um objeto **Field** for definido como true, você poderá usar o método **AppendChunk** para esse campo.</span><span class="sxs-lookup"><span data-stu-id="c2f34-116">If the **adFldLong** bit in the [Attributes](attributes-property-ado.md) property of a **Field** object is set to true, you can use the **AppendChunk** method for that field.</span></span>

<span data-ttu-id="c2f34-p102">A primeira chamada de **AppendChunk** em um objeto **Field** grava dados no campo, substituindo os dados existentes. As chamadas subsequentes de **AppendChunk** são adicionadas aos dados existentes. Se você estiver acrescentando dados a um campo e, em seguida, definir ou ler o valor de outro campo no registro atual, o ADO assumirá que você concluiu o acréscimo de dados ao primeiro campo. Se você chamar o método **AppendChunk** novamente no primeiro campo, o ADO interpretará a chamada como uma nova operação **AppendChunk** e substituirá os dados existentes. O acesso a campos em outros objetos [Recordset](recordset-object-ado.md) que não sejam clones do primeiro objeto **Recordset** não interromperá as operações de **AppendChunk**.</span><span class="sxs-lookup"><span data-stu-id="c2f34-p102">The first **AppendChunk** call on a **Field** object writes data to the field, overwriting any existing data. Subsequent **AppendChunk** calls add to existing data. If you are appending data to one field and then you set or read the value of another field in the current record, ADO assumes that you are finished appending data to the first field. If you call the **AppendChunk** method on the first field again, ADO interprets the call as a new **AppendChunk** operation and overwrites the existing data. Accessing fields in other [Recordset](recordset-object-ado.md) objects that are not clones of the first **Recordset** object will not disrupt **AppendChunk** operations.</span></span>

<span data-ttu-id="c2f34-122">Um erro ocorrerá se não houver registro atual quando você chamar **AppendChunk** em um objeto **Field**.</span><span class="sxs-lookup"><span data-stu-id="c2f34-122">If there is no current record when you call **AppendChunk** on a **Field** object, an error occurs.</span></span>


> [!NOTE]
> <span data-ttu-id="c2f34-p103">[!OBSERVAçãO] O método **AppendChunk** não é operado nos objeto **Field** de um objeto [Record](record-object-ado.md). Ele não executa nenhuma operação e produzirá um erro em tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="c2f34-p103">The **AppendChunk** method does not operate on **Field** objects of a [Record](record-object-ado.md) object. It does not perform any operation and will produce a run-time error.</span></span>



<span data-ttu-id="c2f34-125">**Objeto Parameter**</span><span class="sxs-lookup"><span data-stu-id="c2f34-125">**Parameter**</span></span>

<span data-ttu-id="c2f34-126">Se o bit **adParamLong** na propriedade **Attributes** de um objeto **Parameter** for definido como true, você poderá usar o método **AppendChunk** para esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="c2f34-126">If the **adParamLong** bit in the **Attributes** property of a **Parameter** object is set to true, you can use the **AppendChunk** method for that parameter.</span></span>

<span data-ttu-id="c2f34-p104">A primeira chamada de **AppendChunk** em um objeto **Parameter** grava dados no parâmetro, substituindo os dados existentes. As chamadas subsequentes de **AppendChunk** em um objeto **Parameter** são adicionadas aos dados de parâmetro existentes. A chamada de **AppendChunk** que passar um valor nulo descartará todos os dados de parâmetro.</span><span class="sxs-lookup"><span data-stu-id="c2f34-p104">The first **AppendChunk** call on a **Parameter** object writes data to the parameter, overwriting any existing data. Subsequent **AppendChunk** calls on a **Parameter** object add to existing parameter data. An **AppendChunk** call that passes a null value discards all of the parameter data.</span></span>

