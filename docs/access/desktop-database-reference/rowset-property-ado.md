---
title: Propriedade Rowset (ADO)
TOCTitle: Rowset Property (ADO)
ms:assetid: 1a1cb3ef-8f3c-30c1-3eb0-8618fdcacd53
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248946(v=office.15)
ms:contentKeyID: 48543515
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 95a33fb3d24e5cdbf608d268781be0dd536fa315
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25463676"
---
# <a name="rowset-property-ado"></a><span data-ttu-id="5f743-102">Propriedade Rowset (ADO)</span><span class="sxs-lookup"><span data-stu-id="5f743-102">Rowset Property (ADO)</span></span>


<span data-ttu-id="5f743-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="5f743-103">**Applies to**: Access 2013 | Office 2013</span></span>



<span data-ttu-id="5f743-104">Obtém ou define um objeto **Rowset** do OLE DB a partir de/em um objeto **ADORecordsetConstruction**.</span><span class="sxs-lookup"><span data-stu-id="5f743-104">Gets or sets an OLE DB **Rowset** object from/on an **ADORecordsetConstruction** object.</span></span> <span data-ttu-id="5f743-105">Quando você usa put\_Rowset, o conjunto de linhas seja transformado em um objeto **Recordset** do ADO.</span><span class="sxs-lookup"><span data-stu-id="5f743-105">When you use put\_Rowset, the rowset is turned into an ADO **Recordset** object.</span></span>

<span data-ttu-id="5f743-106">Leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="5f743-106">Read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="5f743-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5f743-107">Syntax</span></span>

<span data-ttu-id="5f743-108">Get HRESULT\_Rowset (\[check-out, retval\] IUnknown\* \* ppRowset);</span><span class="sxs-lookup"><span data-stu-id="5f743-108">HRESULT get\_Rowset(\[out, retval\] IUnknown\*\* ppRowset);</span></span>

<span data-ttu-id="5f743-109">Colocar HRESULT\_Rowset (\[na\] IUnknown\* pRowset);</span><span class="sxs-lookup"><span data-stu-id="5f743-109">HRESULT put\_Rowset(\[in\] IUnknown\* pRowset);</span></span>

## <a name="parameters"></a><span data-ttu-id="5f743-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5f743-110">Parameters</span></span>

  - <span data-ttu-id="5f743-111">*ppRowset*</span><span class="sxs-lookup"><span data-stu-id="5f743-111">*ppRowset*</span></span>

  - <span data-ttu-id="5f743-112">Ponteiro para um objeto **Rowset** do OLE DB.</span><span class="sxs-lookup"><span data-stu-id="5f743-112">Pointer to an OLE DB **Rowset** object.</span></span>

  - <span data-ttu-id="5f743-113">*PRowset*</span><span class="sxs-lookup"><span data-stu-id="5f743-113">*PRowset*</span></span>

  - <span data-ttu-id="5f743-114">Um objeto **Rowset** do OLE DB.</span><span class="sxs-lookup"><span data-stu-id="5f743-114">An OLE DB **Rowset** object.</span></span>

## <a name="return-values"></a><span data-ttu-id="5f743-115">Valores de retorno</span><span class="sxs-lookup"><span data-stu-id="5f743-115">Return Values</span></span>

<span data-ttu-id="5f743-116">Esse método de propriedade retorna os valores padrão HRESULT, incluindo S\_Okey e f\_falhar.</span><span class="sxs-lookup"><span data-stu-id="5f743-116">This property method returns the standard HRESULT values, including S\_OK and E\_FAIL.</span></span>

## <a name="applies-to"></a><span data-ttu-id="5f743-117">Aplica-se a</span><span class="sxs-lookup"><span data-stu-id="5f743-117">Applies To</span></span>

[<span data-ttu-id="5f743-118">ADORecordsetConstruction</span><span class="sxs-lookup"><span data-stu-id="5f743-118">ADORecordsetConstruction</span></span>](adorecordsetconstruction-interface-ado.md)

