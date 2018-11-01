---
title: Linha de propriedade - ActiveX Data Objects (ADO)
TOCTitle: Row property (ADO)
ms:assetid: 1c2b0e27-7232-4b1c-826c-9dc15d758851
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248959(v=office.15)
ms:contentKeyID: 48543562
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 7578a00719946450e840080c21284784a27be170
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25870944"
---
# <a name="row-property-ado"></a><span data-ttu-id="e9289-102">Propriedade Row (ADO)</span><span class="sxs-lookup"><span data-stu-id="e9289-102">Row property (ADO)</span></span>


<span data-ttu-id="e9289-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="e9289-103">**Applies to**: Access 2013, Office 2013</span></span>



<span data-ttu-id="e9289-104">Obtém ou define um objeto **Row** do OLE DB a partir de/em um objeto **ADORecordConstruction**.</span><span class="sxs-lookup"><span data-stu-id="e9289-104">Gets or sets an OLE DB **Row** object from/on an **ADORecordConstruction** object.</span></span> <span data-ttu-id="e9289-105">Quando você usa **colocar\_linha** para definir um objeto **Row** , uma linha seja transformada em um objeto **Record** do ADO.</span><span class="sxs-lookup"><span data-stu-id="e9289-105">When you use **put\_Row** to set a **Row** object, a row is turned into an ADO **Record** object.</span></span> <span data-ttu-id="e9289-106">Leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="e9289-106">Read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="e9289-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e9289-107">Syntax</span></span>

<span data-ttu-id="e9289-108">Get HRESULT\_linha (\[check-out, retval\] IUnknown\* \* ppRow);</span><span class="sxs-lookup"><span data-stu-id="e9289-108">HRESULT get\_Row(\[out, retval\] IUnknown\*\* ppRow);</span></span>

<span data-ttu-id="e9289-109">Colocar HRESULT\_linha (\[na\] IUnknown\* pRow);</span><span class="sxs-lookup"><span data-stu-id="e9289-109">HRESULT put\_Row(\[in\] IUnknown\* pRow);</span></span>

## <a name="parameters"></a><span data-ttu-id="e9289-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e9289-110">Parameters</span></span>

  - <span data-ttu-id="e9289-111">*ppRow*</span><span class="sxs-lookup"><span data-stu-id="e9289-111">*ppRow*</span></span>

  - <span data-ttu-id="e9289-112">Ponteiro para um objeto **Row** do OLE DB.</span><span class="sxs-lookup"><span data-stu-id="e9289-112">Pointer to an OLE DB **Row** object.</span></span>

  - <span data-ttu-id="e9289-113">*PRow*</span><span class="sxs-lookup"><span data-stu-id="e9289-113">*PRow*</span></span>

  - <span data-ttu-id="e9289-114">Um objeto **Row** do OLE DB.</span><span class="sxs-lookup"><span data-stu-id="e9289-114">An OLE DB **Row** object.</span></span>

## <a name="return-values"></a><span data-ttu-id="e9289-115">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="e9289-115">Return values</span></span>

<span data-ttu-id="e9289-116">Esse método de propriedade retorna os valores padrão HRESULT, incluindo S\_Okey e f\_falhar.</span><span class="sxs-lookup"><span data-stu-id="e9289-116">This property method returns the standard HRESULT values, including S\_OK and E\_FAIL.</span></span>

## <a name="applies-to"></a><span data-ttu-id="e9289-117">Aplica-se a</span><span class="sxs-lookup"><span data-stu-id="e9289-117">Applies To</span></span>

[<span data-ttu-id="e9289-118">ADORecordConstruction</span><span class="sxs-lookup"><span data-stu-id="e9289-118">ADORecordConstruction</span></span>](adorecordconstruction-interface-ado.md)

