---
title: Linha de propriedade - ActiveX Data Objects (ADO)
TOCTitle: Row property (ADO)
ms:assetid: 1c2b0e27-7232-4b1c-826c-9dc15d758851
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248959(v=office.15)
ms:contentKeyID: 48543562
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 1882486de2a2dfe61b98d4461abeea9cbcc23363
ms.sourcegitcommit: 980a96cf444882d3d34cecb5faac8f8a7b7c4b57
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/03/2018
ms.locfileid: "25949310"
---
# <a name="row-property-ado"></a><span data-ttu-id="00b31-102">Propriedade Row (ADO)</span><span class="sxs-lookup"><span data-stu-id="00b31-102">Row property (ADO)</span></span>

<span data-ttu-id="00b31-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="00b31-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="00b31-104">Obtém ou define um objeto **Row** do OLE DB a partir de/em um objeto **ADORecordConstruction**.</span><span class="sxs-lookup"><span data-stu-id="00b31-104">Gets or sets an OLE DB **Row** object from/on an **ADORecordConstruction** object.</span></span> <span data-ttu-id="00b31-105">Quando você usa **colocar\_linha** para definir um objeto **Row** , uma linha seja transformada em um objeto **Record** do ADO.</span><span class="sxs-lookup"><span data-stu-id="00b31-105">When you use **put\_Row** to set a **Row** object, a row is turned into an ADO **Record** object.</span></span> <span data-ttu-id="00b31-106">Leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="00b31-106">Read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="00b31-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="00b31-107">Syntax</span></span>

<span data-ttu-id="00b31-108">Get HRESULT\_linha (\[check-out, retval\] IUnknown\* \* ppRow);</span><span class="sxs-lookup"><span data-stu-id="00b31-108">HRESULT get\_Row(\[out, retval\] IUnknown\*\* ppRow);</span></span>

<span data-ttu-id="00b31-109">Colocar HRESULT\_linha (\[na\] IUnknown\* pRow);</span><span class="sxs-lookup"><span data-stu-id="00b31-109">HRESULT put\_Row(\[in\] IUnknown\* pRow);</span></span>

## <a name="parameters"></a><span data-ttu-id="00b31-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="00b31-110">Parameters</span></span>

|<span data-ttu-id="00b31-111">Parâmetro</span><span class="sxs-lookup"><span data-stu-id="00b31-111">Parameter</span></span>|<span data-ttu-id="00b31-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="00b31-112">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="00b31-113">*ppRow*</span><span class="sxs-lookup"><span data-stu-id="00b31-113">*ppRow*</span></span> |<span data-ttu-id="00b31-114">Ponteiro para um objeto **Row** do OLE DB.</span><span class="sxs-lookup"><span data-stu-id="00b31-114">Pointer to an OLE DB **Row** object.</span></span>|
|<span data-ttu-id="00b31-115">*PRow*</span><span class="sxs-lookup"><span data-stu-id="00b31-115">*PRow*</span></span> |<span data-ttu-id="00b31-116">Um objeto **Row** do OLE DB.</span><span class="sxs-lookup"><span data-stu-id="00b31-116">An OLE DB **Row** object.</span></span>|

## <a name="return-values"></a><span data-ttu-id="00b31-117">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="00b31-117">Return values</span></span>

<span data-ttu-id="00b31-118">Esse método de propriedade retorna os valores padrão HRESULT, incluindo S\_Okey e f\_falhar.</span><span class="sxs-lookup"><span data-stu-id="00b31-118">This property method returns the standard HRESULT values, including S\_OK and E\_FAIL.</span></span>

## <a name="applies-to"></a><span data-ttu-id="00b31-119">Aplica-se a</span><span class="sxs-lookup"><span data-stu-id="00b31-119">Applies to</span></span>

[<span data-ttu-id="00b31-120">ADORecordConstruction</span><span class="sxs-lookup"><span data-stu-id="00b31-120">ADORecordConstruction</span></span>](adorecordconstruction-interface-ado.md)

