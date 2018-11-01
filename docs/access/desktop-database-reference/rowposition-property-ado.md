---
title: Propriedade RowPosition (ADO)
TOCTitle: RowPosition property (ADO)
ms:assetid: b87f14b0-136b-0564-3e12-f9d5ecc4f7c8
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249887(v=office.15)
ms:contentKeyID: 48547325
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 6f83d1b113b29be06ffded5263791d3db3068f7f
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25869068"
---
# <a name="rowposition-property-ado"></a><span data-ttu-id="81037-102">Propriedade RowPosition (ADO)</span><span class="sxs-lookup"><span data-stu-id="81037-102">RowPosition property (ADO)</span></span>


<span data-ttu-id="81037-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="81037-103">**Applies to**: Access 2013, Office 2013</span></span>



<span data-ttu-id="81037-104">Obtém ou define um objeto **RowPosition** do OLE DB a partir de/em um objeto **ADORecordsetConstruction**.</span><span class="sxs-lookup"><span data-stu-id="81037-104">Gets or sets an OLE DB **RowPosition** object from/on an **ADORecordsetConstruction** object.</span></span> <span data-ttu-id="81037-105">Quando você usa **colocar\_RowPosition** para definir o objeto **RowPosition** , o objeto **Recordset** resultante usa o objeto **RowPosition** para determinar a linha atual.</span><span class="sxs-lookup"><span data-stu-id="81037-105">When you use **put\_RowPosition** to set the **RowPosition** object, the resulting **Recordset** object uses the **RowPosition** object to determine the current row.</span></span>

<span data-ttu-id="81037-106">Leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="81037-106">Read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="81037-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="81037-107">Syntax</span></span>

<span data-ttu-id="81037-108">Get HRESULT\_RowPosition (\[check-out, retval\] IUnknown\* \* ppRowPos);</span><span class="sxs-lookup"><span data-stu-id="81037-108">HRESULT get\_RowPosition(\[out, retval\] IUnknown\*\* ppRowPos);</span></span>

<span data-ttu-id="81037-109">Colocar HRESULT\_RowPosition (\[na\] IUnknown\* pRowPos);</span><span class="sxs-lookup"><span data-stu-id="81037-109">HRESULT put\_RowPosition(\[in\] IUnknown\* pRowPos);</span></span>

## <a name="parameters"></a><span data-ttu-id="81037-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="81037-110">Parameters</span></span>

  - <span data-ttu-id="81037-111">*ppRowPos*</span><span class="sxs-lookup"><span data-stu-id="81037-111">*ppRowPos*</span></span>

  - <span data-ttu-id="81037-112">Ponteiro para um objeto **RowPosition** do OLE DB.</span><span class="sxs-lookup"><span data-stu-id="81037-112">Pointer to an OLE DB **RowPosition** object.</span></span>

  - <span data-ttu-id="81037-113">*PRowPos*</span><span class="sxs-lookup"><span data-stu-id="81037-113">*PRowPos*</span></span>

  - <span data-ttu-id="81037-114">Um objeto **RowPosition** do OLE DB.</span><span class="sxs-lookup"><span data-stu-id="81037-114">An OLE DB **RowPosition** object.</span></span>

## <a name="return-values"></a><span data-ttu-id="81037-115">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="81037-115">Return values</span></span>

<span data-ttu-id="81037-116">Esse método de propriedade retorna os valores padrão HRESULT, incluindo S\_Okey e f\_falhar.</span><span class="sxs-lookup"><span data-stu-id="81037-116">This property method returns the standard HRESULT values, including S\_OK and E\_FAIL.</span></span>

## <a name="remarks"></a><span data-ttu-id="81037-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="81037-117">Remarks</span></span>

<span data-ttu-id="81037-p102">Quando esta propriedade for definida, se o objeto **Rowset** no objeto **RowPosition** for diferente do objeto **Rowset** no objeto **Recordset**, o primeiro substituirá o segundo. O mesmo comportamento também se aplicará ao **Charter** atual do **RowPosition**.</span><span class="sxs-lookup"><span data-stu-id="81037-p102">When this property is set, if the **Rowset** object on the **RowPosition** object is different from the **Rowset** object on the **Recordset** object, the former overrides the latter. The same behavior applies to the current **Chapter** of the **RowPosition** as well.</span></span>

## <a name="applies-to"></a><span data-ttu-id="81037-120">Aplica-se a</span><span class="sxs-lookup"><span data-stu-id="81037-120">Applies To</span></span>

[<span data-ttu-id="81037-121">ADORecordsetConstruction</span><span class="sxs-lookup"><span data-stu-id="81037-121">ADORecordsetConstruction</span></span>](adorecordsetconstruction-interface-ado.md)

