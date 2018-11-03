---
title: Propriedade Chapter (ADO)
TOCTitle: Chapter property (ADO)
ms:assetid: d7c9478e-487f-7023-1dd8-5313433dbc5e
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250085(v=office.15)
ms:contentKeyID: 48548014
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 95ed1b9b7c048353950b2481c7fefe2211b2799b
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/03/2018
ms.locfileid: "25944274"
---
# <a name="chapter-property-ado"></a><span data-ttu-id="dfaf9-102">Propriedade Chapter (ADO)</span><span class="sxs-lookup"><span data-stu-id="dfaf9-102">Chapter property (ADO)</span></span>


<span data-ttu-id="dfaf9-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="dfaf9-103">**Applies to**: Access 2013, Office 2013</span></span>
 

<span data-ttu-id="dfaf9-104">Obtém ou configura um objeto **Chapter** do OLE DB de/em um objeto **ADORecordsetConstruction**.</span><span class="sxs-lookup"><span data-stu-id="dfaf9-104">Gets or sets an OLE DB **Chapter** object from/on an **ADORecordsetConstruction** object.</span></span> <span data-ttu-id="dfaf9-105">Quando você usa **colocar\_capítulo** para definir o objeto de **capítulo** , um subconjunto de linhas seja transformado em um objeto **Recordset** do ADO.</span><span class="sxs-lookup"><span data-stu-id="dfaf9-105">When you use **put\_Chapter** to set the **Chapter** object, a subset of rows is turned into an ADO **Recordset** object.</span></span> <span data-ttu-id="dfaf9-106">Isso define o capítulo atual do objeto **Rowset**.</span><span class="sxs-lookup"><span data-stu-id="dfaf9-106">This sets the current chapter of the **Rowset** object.</span></span> <span data-ttu-id="dfaf9-107">Leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="dfaf9-107">Read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="dfaf9-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="dfaf9-108">Syntax</span></span>

<span data-ttu-id="dfaf9-109">Get HRESULT\_capítulo (\[check-out, retval\] longo\* plChapter);</span><span class="sxs-lookup"><span data-stu-id="dfaf9-109">HRESULT get\_Chapter(\[out, retval\] long\* plChapter);</span></span>

<span data-ttu-id="dfaf9-110">Colocar HRESULT\_capítulo (\[na\] lChapter longo);</span><span class="sxs-lookup"><span data-stu-id="dfaf9-110">HRESULT put\_Chapter(\[in\] long lChapter);</span></span>

## <a name="parameters"></a><span data-ttu-id="dfaf9-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="dfaf9-111">Parameters</span></span>

- <span data-ttu-id="dfaf9-112">*plChapter*</span><span class="sxs-lookup"><span data-stu-id="dfaf9-112">*plChapter*</span></span>

  - <span data-ttu-id="dfaf9-113">Ponteiro para o identificador de um capítulo.</span><span class="sxs-lookup"><span data-stu-id="dfaf9-113">Pointer to the handle of a chapter.</span></span>

- <span data-ttu-id="dfaf9-114">*LChapter*</span><span class="sxs-lookup"><span data-stu-id="dfaf9-114">*LChapter*</span></span>

  - <span data-ttu-id="dfaf9-115">Identificador de um capítulo.</span><span class="sxs-lookup"><span data-stu-id="dfaf9-115">Handle of a chapter.</span></span>

## <a name="return-values"></a><span data-ttu-id="dfaf9-116">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="dfaf9-116">Return values</span></span>

<span data-ttu-id="dfaf9-117">Esse método de propriedade retorna os valores padrão HRESULT, incluindo S\_Okey e f\_falhar.</span><span class="sxs-lookup"><span data-stu-id="dfaf9-117">This property method returns the standard HRESULT values, including S\_OK and E\_FAIL.</span></span>

## <a name="applies-to"></a><span data-ttu-id="dfaf9-118">Aplica-se a</span><span class="sxs-lookup"><span data-stu-id="dfaf9-118">Applies To</span></span>

[<span data-ttu-id="dfaf9-119">ADORecordsetConstruction</span><span class="sxs-lookup"><span data-stu-id="dfaf9-119">ADORecordsetConstruction</span></span>](adorecordsetconstruction-interface-ado.md)

