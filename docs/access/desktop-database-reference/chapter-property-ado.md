---
title: Propriedade Chapter (ADO)
TOCTitle: Chapter Property (ADO)
ms:assetid: d7c9478e-487f-7023-1dd8-5313433dbc5e
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250085(v=office.15)
ms:contentKeyID: 48548014
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: f02b20aef2b76ff00ce23b8597132dc22b414993
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25464538"
---
# <a name="chapter-property-ado"></a><span data-ttu-id="54c2d-102">Propriedade Chapter (ADO)</span><span class="sxs-lookup"><span data-stu-id="54c2d-102">Chapter Property (ADO)</span></span>


<span data-ttu-id="54c2d-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="54c2d-103">**Applies to**: Access 2013 | Office 2013</span></span>
 

<span data-ttu-id="54c2d-104">Obtém ou configura um objeto **Chapter** do OLE DB de/em um objeto **ADORecordsetConstruction**.</span><span class="sxs-lookup"><span data-stu-id="54c2d-104">Gets or sets an OLE DB **Chapter** object from/on an **ADORecordsetConstruction** object.</span></span> <span data-ttu-id="54c2d-105">Quando você usa **colocar\_capítulo** para definir o objeto de **capítulo** , um subconjunto de linhas seja transformado em um objeto **Recordset** do ADO.</span><span class="sxs-lookup"><span data-stu-id="54c2d-105">When you use **put\_Chapter** to set the **Chapter** object, a subset of rows is turned into an ADO **Recordset** object.</span></span> <span data-ttu-id="54c2d-106">Isso define o capítulo atual do objeto **Rowset**.</span><span class="sxs-lookup"><span data-stu-id="54c2d-106">This sets the current chapter of the **Rowset** object.</span></span> <span data-ttu-id="54c2d-107">Leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="54c2d-107">Read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="54c2d-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="54c2d-108">Syntax</span></span>

<span data-ttu-id="54c2d-109">Get HRESULT\_capítulo (\[check-out, retval\] longo\* plChapter);</span><span class="sxs-lookup"><span data-stu-id="54c2d-109">HRESULT get\_Chapter(\[out, retval\] long\* plChapter);</span></span>

<span data-ttu-id="54c2d-110">Colocar HRESULT\_capítulo (\[na\] lChapter longo);</span><span class="sxs-lookup"><span data-stu-id="54c2d-110">HRESULT put\_Chapter(\[in\] long lChapter);</span></span>

## <a name="parameters"></a><span data-ttu-id="54c2d-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="54c2d-111">Parameters</span></span>

  - <span data-ttu-id="54c2d-112">*plChapter*</span><span class="sxs-lookup"><span data-stu-id="54c2d-112">*plChapter*</span></span>

  - <span data-ttu-id="54c2d-113">Ponteiro para o identificador de um capítulo.</span><span class="sxs-lookup"><span data-stu-id="54c2d-113">Pointer to the handle of a chapter.</span></span>

  - <span data-ttu-id="54c2d-114">*LChapter*</span><span class="sxs-lookup"><span data-stu-id="54c2d-114">*LChapter*</span></span>

  - <span data-ttu-id="54c2d-115">Identificador de um capítulo.</span><span class="sxs-lookup"><span data-stu-id="54c2d-115">Handle of a chapter.</span></span>

## <a name="return-values"></a><span data-ttu-id="54c2d-116">Valores de retorno</span><span class="sxs-lookup"><span data-stu-id="54c2d-116">Return Values</span></span>

<span data-ttu-id="54c2d-117">Esse método de propriedade retorna os valores padrão HRESULT, incluindo S\_Okey e f\_falhar.</span><span class="sxs-lookup"><span data-stu-id="54c2d-117">This property method returns the standard HRESULT values, including S\_OK and E\_FAIL.</span></span>

## <a name="applies-to"></a><span data-ttu-id="54c2d-118">Aplica-se a</span><span class="sxs-lookup"><span data-stu-id="54c2d-118">Applies To</span></span>

[<span data-ttu-id="54c2d-119">ADORecordsetConstruction</span><span class="sxs-lookup"><span data-stu-id="54c2d-119">ADORecordsetConstruction</span></span>](adorecordsetconstruction-interface-ado.md)

