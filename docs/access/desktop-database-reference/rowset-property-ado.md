---
title: Propriedade Rowset (ADO)
TOCTitle: Rowset property (ADO)
ms:assetid: 1a1cb3ef-8f3c-30c1-3eb0-8618fdcacd53
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248946(v=office.15)
ms:contentKeyID: 48543515
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 7be8abbce6828dd202e0c64eec342de9198f7a9b
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25878532"
---
# <a name="rowset-property-ado"></a><span data-ttu-id="27579-102">Propriedade Rowset (ADO)</span><span class="sxs-lookup"><span data-stu-id="27579-102">Rowset property (ADO)</span></span>


<span data-ttu-id="27579-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="27579-103">**Applies to**: Access 2013, Office 2013</span></span>



<span data-ttu-id="27579-104">Obtém ou define um objeto **Rowset** do OLE DB a partir de/em um objeto **ADORecordsetConstruction**.</span><span class="sxs-lookup"><span data-stu-id="27579-104">Gets or sets an OLE DB **Rowset** object from/on an **ADORecordsetConstruction** object.</span></span> <span data-ttu-id="27579-105">Quando você usa put\_Rowset, o conjunto de linhas seja transformado em um objeto **Recordset** do ADO.</span><span class="sxs-lookup"><span data-stu-id="27579-105">When you use put\_Rowset, the rowset is turned into an ADO **Recordset** object.</span></span>

<span data-ttu-id="27579-106">Leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="27579-106">Read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="27579-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="27579-107">Syntax</span></span>

<span data-ttu-id="27579-108">Get HRESULT\_Rowset (\[check-out, retval\] IUnknown\* \* ppRowset);</span><span class="sxs-lookup"><span data-stu-id="27579-108">HRESULT get\_Rowset(\[out, retval\] IUnknown\*\* ppRowset);</span></span>

<span data-ttu-id="27579-109">Colocar HRESULT\_Rowset (\[na\] IUnknown\* pRowset);</span><span class="sxs-lookup"><span data-stu-id="27579-109">HRESULT put\_Rowset(\[in\] IUnknown\* pRowset);</span></span>

## <a name="parameters"></a><span data-ttu-id="27579-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="27579-110">Parameters</span></span>

  - <span data-ttu-id="27579-111">*ppRowset*</span><span class="sxs-lookup"><span data-stu-id="27579-111">*ppRowset*</span></span>

  - <span data-ttu-id="27579-112">Ponteiro para um objeto **Rowset** do OLE DB.</span><span class="sxs-lookup"><span data-stu-id="27579-112">Pointer to an OLE DB **Rowset** object.</span></span>

  - <span data-ttu-id="27579-113">*PRowset*</span><span class="sxs-lookup"><span data-stu-id="27579-113">*PRowset*</span></span>

  - <span data-ttu-id="27579-114">Um objeto **Rowset** do OLE DB.</span><span class="sxs-lookup"><span data-stu-id="27579-114">An OLE DB **Rowset** object.</span></span>

## <a name="return-values"></a><span data-ttu-id="27579-115">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="27579-115">Return values</span></span>

<span data-ttu-id="27579-116">Esse método de propriedade retorna os valores padrão HRESULT, incluindo S\_Okey e f\_falhar.</span><span class="sxs-lookup"><span data-stu-id="27579-116">This property method returns the standard HRESULT values, including S\_OK and E\_FAIL.</span></span>

## <a name="applies-to"></a><span data-ttu-id="27579-117">Aplica-se a</span><span class="sxs-lookup"><span data-stu-id="27579-117">Applies To</span></span>

[<span data-ttu-id="27579-118">ADORecordsetConstruction</span><span class="sxs-lookup"><span data-stu-id="27579-118">ADORecordsetConstruction</span></span>](adorecordsetconstruction-interface-ado.md)

