---
title: Propriedade Chapter (ADO)
TOCTitle: Chapter property (ADO)
ms:assetid: d7c9478e-487f-7023-1dd8-5313433dbc5e
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250085(v=office.15)
ms:contentKeyID: 48548014
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: b4f4efc2ffab9f7996b2d805658b985badbaf87e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296392"
---
# <a name="chapter-property-ado"></a><span data-ttu-id="56473-102">Propriedade Chapter (ADO)</span><span class="sxs-lookup"><span data-stu-id="56473-102">Chapter property (ADO)</span></span>

<span data-ttu-id="56473-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="56473-103">**Applies to**: Access 2013, Office 2013</span></span>
 
<span data-ttu-id="56473-104">Obtém ou configura um objeto **Chapter** do OLE DB de/em um objeto **ADORecordsetConstruction**.</span><span class="sxs-lookup"><span data-stu-id="56473-104">Gets or sets an OLE DB **Chapter** object from/on an **ADORecordsetConstruction** object.</span></span> <span data-ttu-id="56473-105">Quando você usa **colocar \_ Chapter** para definir o objeto **Chapter,** um subconjunto de linhas é transformado em um objeto **Recordset do** ADO.</span><span class="sxs-lookup"><span data-stu-id="56473-105">When you use **put\_Chapter** to set the **Chapter** object, a subset of rows is turned into an ADO **Recordset** object.</span></span> <span data-ttu-id="56473-106">Isso define o capítulo atual do objeto **Rowset**.</span><span class="sxs-lookup"><span data-stu-id="56473-106">This sets the current chapter of the **Rowset** object.</span></span> <span data-ttu-id="56473-107">Leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="56473-107">Read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="56473-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="56473-108">Syntax</span></span>

<span data-ttu-id="56473-109">HRESULT get \_ Chapter( \[ out, retval \] long \* plChapter);</span><span class="sxs-lookup"><span data-stu-id="56473-109">HRESULT get\_Chapter(\[out, retval\] long\* plChapter);</span></span>

<span data-ttu-id="56473-110">HRESULT put \_ Chapter( \[ in long \] lChapter);</span><span class="sxs-lookup"><span data-stu-id="56473-110">HRESULT put\_Chapter(\[in\] long lChapter);</span></span>

## <a name="parameters"></a><span data-ttu-id="56473-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="56473-111">Parameters</span></span>

|<span data-ttu-id="56473-112">Parâmetro</span><span class="sxs-lookup"><span data-stu-id="56473-112">Parameter</span></span>|<span data-ttu-id="56473-113">Descrição</span><span class="sxs-lookup"><span data-stu-id="56473-113">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="56473-114">*plChapter*</span><span class="sxs-lookup"><span data-stu-id="56473-114">*plChapter*</span></span> |<span data-ttu-id="56473-115">Ponteiro para o identificador de um capítulo.</span><span class="sxs-lookup"><span data-stu-id="56473-115">Pointer to the handle of a chapter.</span></span>|
|<span data-ttu-id="56473-116">*LChapter*</span><span class="sxs-lookup"><span data-stu-id="56473-116">*LChapter*</span></span> |<span data-ttu-id="56473-117">Identificador de um capítulo.</span><span class="sxs-lookup"><span data-stu-id="56473-117">Handle of a chapter.</span></span>|

## <a name="return-values"></a><span data-ttu-id="56473-118">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="56473-118">Return values</span></span>

<span data-ttu-id="56473-119">Esse método de propriedade retorna os valores HRESULT padrão, incluindo S \_ OK e E \_ FAIL.</span><span class="sxs-lookup"><span data-stu-id="56473-119">This property method returns the standard HRESULT values, including S\_OK and E\_FAIL.</span></span>

## <a name="applies-to"></a><span data-ttu-id="56473-120">Aplica-se a</span><span class="sxs-lookup"><span data-stu-id="56473-120">Applies To</span></span>

[<span data-ttu-id="56473-121">ADORecordsetConstruction</span><span class="sxs-lookup"><span data-stu-id="56473-121">ADORecordsetConstruction</span></span>](adorecordsetconstruction-interface-ado.md)

