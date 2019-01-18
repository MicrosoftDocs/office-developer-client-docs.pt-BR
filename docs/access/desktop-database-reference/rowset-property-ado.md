---
title: Propriedade Rowset (ADO)
TOCTitle: Rowset property (ADO)
ms:assetid: 1a1cb3ef-8f3c-30c1-3eb0-8618fdcacd53
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248946(v=office.15)
ms:contentKeyID: 48543515
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: be2a4855b3411a11ddd5a76225acaa52344877a4
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28706139"
---
# <a name="rowset-property-ado"></a><span data-ttu-id="e5ff5-102">Propriedade Rowset (ADO)</span><span class="sxs-lookup"><span data-stu-id="e5ff5-102">Rowset property (ADO)</span></span>

<span data-ttu-id="e5ff5-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="e5ff5-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="e5ff5-104">Obtém ou define um objeto **Rowset** do OLE DB a partir de/em um objeto **ADORecordsetConstruction**.</span><span class="sxs-lookup"><span data-stu-id="e5ff5-104">Gets or sets an OLE DB **Rowset** object from/on an **ADORecordsetConstruction** object.</span></span> <span data-ttu-id="e5ff5-105">Quando você usa put\_Rowset, o conjunto de linhas seja transformado em um objeto **Recordset** do ADO.</span><span class="sxs-lookup"><span data-stu-id="e5ff5-105">When you use put\_Rowset, the rowset is turned into an ADO **Recordset** object.</span></span>

<span data-ttu-id="e5ff5-106">Leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="e5ff5-106">Read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="e5ff5-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e5ff5-107">Syntax</span></span>

<span data-ttu-id="e5ff5-108">Get HRESULT\_Rowset (\[check-out, retval\] IUnknown\* \* ppRowset);</span><span class="sxs-lookup"><span data-stu-id="e5ff5-108">HRESULT get\_Rowset(\[out, retval\] IUnknown\*\* ppRowset);</span></span>

<span data-ttu-id="e5ff5-109">Colocar HRESULT\_Rowset (\[na\] IUnknown\* pRowset);</span><span class="sxs-lookup"><span data-stu-id="e5ff5-109">HRESULT put\_Rowset(\[in\] IUnknown\* pRowset);</span></span>

## <a name="parameters"></a><span data-ttu-id="e5ff5-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e5ff5-110">Parameters</span></span>

|<span data-ttu-id="e5ff5-111">Parâmetro</span><span class="sxs-lookup"><span data-stu-id="e5ff5-111">Parameter</span></span>|<span data-ttu-id="e5ff5-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="e5ff5-112">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="e5ff5-113">*ppRowset*</span><span class="sxs-lookup"><span data-stu-id="e5ff5-113">*ppRowset*</span></span> |<span data-ttu-id="e5ff5-114">Ponteiro para um objeto **Rowset** do OLE DB.</span><span class="sxs-lookup"><span data-stu-id="e5ff5-114">Pointer to an OLE DB **Rowset** object.</span></span>|
|<span data-ttu-id="e5ff5-115">*PRowset*</span><span class="sxs-lookup"><span data-stu-id="e5ff5-115">*PRowset*</span></span> |<span data-ttu-id="e5ff5-116">Um objeto **Rowset** do OLE DB.</span><span class="sxs-lookup"><span data-stu-id="e5ff5-116">An OLE DB **Rowset** object.</span></span>|

## <a name="return-values"></a><span data-ttu-id="e5ff5-117">Valores de retorno</span><span class="sxs-lookup"><span data-stu-id="e5ff5-117">Return values</span></span>

<span data-ttu-id="e5ff5-118">Esse método de propriedade retorna os valores padrão HRESULT, incluindo S\_Okey e f\_falhar.</span><span class="sxs-lookup"><span data-stu-id="e5ff5-118">This property method returns the standard HRESULT values, including S\_OK and E\_FAIL.</span></span>

## <a name="applies-to"></a><span data-ttu-id="e5ff5-119">Aplica-se a</span><span class="sxs-lookup"><span data-stu-id="e5ff5-119">Applies to</span></span>

[<span data-ttu-id="e5ff5-120">ADORecordsetConstruction</span><span class="sxs-lookup"><span data-stu-id="e5ff5-120">ADORecordsetConstruction</span></span>](adorecordsetconstruction-interface-ado.md)

