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
description: Abre um arquivo de Ajuda em HTML com a palavra-chave do especificado na caixa Pesquisar.
ms.openlocfilehash: 4671b18333bdae953c487662cd880849233df7f5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772014"
---
# <a name="help-function"></a><span data-ttu-id="3a6d6-103">Função HELP</span><span class="sxs-lookup"><span data-stu-id="3a6d6-103">HELP Function</span></span>

<span data-ttu-id="3a6d6-104">Abre um arquivo de Ajuda em HTML com a *palavra-chave* do especificado na caixa **Pesquisar** .</span><span class="sxs-lookup"><span data-stu-id="3a6d6-104">Opens an HTML Help file with the specifed  *keyword*  in the **Search** box.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="3a6d6-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3a6d6-105">Syntax</span></span>

<span data-ttu-id="3a6d6-106">AJUDAR ("* * *filename.chm!keyword* * *")</span><span class="sxs-lookup"><span data-stu-id="3a6d6-106">HELP(" ** *filename.chm!keyword* ** ")</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="3a6d6-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3a6d6-107">Parameters</span></span>

|<span data-ttu-id="3a6d6-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="3a6d6-108">**Name**</span></span>|<span data-ttu-id="3a6d6-109">**Obrigatório/Opcional**</span><span class="sxs-lookup"><span data-stu-id="3a6d6-109">**Required/Optional**</span></span>|<span data-ttu-id="3a6d6-110">**Tipo de dados**</span><span class="sxs-lookup"><span data-stu-id="3a6d6-110">**Data Type**</span></span>|<span data-ttu-id="3a6d6-111">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="3a6d6-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="3a6d6-112">_filename.chm!Keyword_</span><span class="sxs-lookup"><span data-stu-id="3a6d6-112">_filename.chm!keyword_</span></span> <br/> |<span data-ttu-id="3a6d6-113">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="3a6d6-113">Required</span></span>  <br/> |<span data-ttu-id="3a6d6-114">**String**</span><span class="sxs-lookup"><span data-stu-id="3a6d6-114">**String**</span></span> <br/> | <span data-ttu-id="3a6d6-115">O nome do arquivo da Ajuda e a palavra-chave a ser pesquisada.</span><span class="sxs-lookup"><span data-stu-id="3a6d6-115">The filename of the Help file and the keyword to search for.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3a6d6-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="3a6d6-116">Remarks</span></span>

<span data-ttu-id="3a6d6-117">Se nenhuma *palavra-chave* for especificado, a função HELP abrirá a página de conteúdo do arquivo de Ajuda.</span><span class="sxs-lookup"><span data-stu-id="3a6d6-117">If no  *keyword*  is specified, the HELP function opens the contents page of the Help file.</span></span> 
  
## <a name="example"></a><span data-ttu-id="3a6d6-118">Exemplo</span><span class="sxs-lookup"><span data-stu-id="3a6d6-118">Example</span></span>

<span data-ttu-id="3a6d6-119">Help("Visio.chm!ShapeSheet")</span><span class="sxs-lookup"><span data-stu-id="3a6d6-119">HELP("visio.chm!shapesheet")</span></span> 
  
<span data-ttu-id="3a6d6-120">Abre o arquivo da Ajuda do Visio e exibe uma lista dos tópicos cuja palavra-chave é "shapesheet".</span><span class="sxs-lookup"><span data-stu-id="3a6d6-120">Opens the Visio Help file and displays a list of the topic(s) whose keyword is "shapesheet."</span></span> 
  

