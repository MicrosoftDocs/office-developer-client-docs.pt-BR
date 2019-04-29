---
title: Função HELP
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251436
localization_priority: Normal
ms.assetid: 5b358c38-6ed1-3fbe-c1d1-1a56ebbaa870
description: Abre um arquivo de ajuda HTML com a palavra-chave especificada na caixa de pesquisa.
ms.openlocfilehash: 639d10bf489d1ad09aef1522d3cbc743bbe66f6f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431334"
---
# <a name="help-function"></a><span data-ttu-id="6d30f-103">Função HELP</span><span class="sxs-lookup"><span data-stu-id="6d30f-103">HELP Function</span></span>

<span data-ttu-id="6d30f-104">Abre um arquivo de ajuda HTML com a *palavra-chave* especificada na caixa de **pesquisa** .</span><span class="sxs-lookup"><span data-stu-id="6d30f-104">Opens an HTML Help file with the specifed  *keyword*  in the **Search** box.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="6d30f-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6d30f-105">Syntax</span></span>

<span data-ttu-id="6d30f-106">HELP ("\* \* *filename. chm! keyword* \* \*")</span><span class="sxs-lookup"><span data-stu-id="6d30f-106">HELP(" \*\* *filename.chm!keyword* \*\* ")</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="6d30f-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6d30f-107">Parameters</span></span>

|<span data-ttu-id="6d30f-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="6d30f-108">**Name**</span></span>|<span data-ttu-id="6d30f-109">**Obrigatório/opcional**</span><span class="sxs-lookup"><span data-stu-id="6d30f-109">**Required/Optional**</span></span>|<span data-ttu-id="6d30f-110">**Tipo de dados**</span><span class="sxs-lookup"><span data-stu-id="6d30f-110">**Data Type**</span></span>|<span data-ttu-id="6d30f-111">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="6d30f-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="6d30f-112">_nome de arquivo. chm! palavra-chave_</span><span class="sxs-lookup"><span data-stu-id="6d30f-112">_filename.chm!keyword_</span></span> <br/> |<span data-ttu-id="6d30f-113">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="6d30f-113">Required</span></span>  <br/> |<span data-ttu-id="6d30f-114">**Cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="6d30f-114">**String**</span></span> <br/> | <span data-ttu-id="6d30f-115">O nome do arquivo da Ajuda e a palavra-chave a ser pesquisada.</span><span class="sxs-lookup"><span data-stu-id="6d30f-115">The filename of the Help file and the keyword to search for.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6d30f-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="6d30f-116">Remarks</span></span>

<span data-ttu-id="6d30f-117">Se nenhuma *palavra-chave* for especificada, a função ajuda abrirá a página conteúdo do arquivo de ajuda.</span><span class="sxs-lookup"><span data-stu-id="6d30f-117">If no  *keyword*  is specified, the HELP function opens the contents page of the Help file.</span></span> 
  
## <a name="example"></a><span data-ttu-id="6d30f-118">Exemplo</span><span class="sxs-lookup"><span data-stu-id="6d30f-118">Example</span></span>

<span data-ttu-id="6d30f-119">AJUDA ("Visio. chm! ShapeSheet")</span><span class="sxs-lookup"><span data-stu-id="6d30f-119">HELP("visio.chm!shapesheet")</span></span> 
  
<span data-ttu-id="6d30f-120">Abre o arquivo da Ajuda do Visio e exibe uma lista dos tópicos cuja palavra-chave é "shapesheet".</span><span class="sxs-lookup"><span data-stu-id="6d30f-120">Opens the Visio Help file and displays a list of the topic(s) whose keyword is "shapesheet."</span></span> 
  

