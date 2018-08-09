---
title: Implementar verbos de formulário padrão
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: f89f7c58-6358-4523-9788-676f189b5e69
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 8135af7947f30ac600b8d9af364b2a79a3443ab6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767446"
---
# <a name="implementing-standard-form-verbs"></a><span data-ttu-id="352b2-103">Implementar verbos de formulário padrão</span><span class="sxs-lookup"><span data-stu-id="352b2-103">Implementing Standard Form Verbs</span></span>

  
  
<span data-ttu-id="352b2-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="352b2-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="352b2-105">MAPI define um conjunto de verbos padrão ou ações tomadas quando um usuário faz uma seleção de menu ou clicar em um botão, que devem oferecer suporte a todos os visualizadores de formulário.</span><span class="sxs-lookup"><span data-stu-id="352b2-105">MAPI defines a set of standard verbs, or actions taken when a user makes a menu selection or clicks a button, that all form viewers should support.</span></span> <span data-ttu-id="352b2-106">Cada verbo tem uma constante associada a ela para identificação, definida no EXCHFORM. Arquivo de cabeçalho H.</span><span class="sxs-lookup"><span data-stu-id="352b2-106">Each verb has a constant associated with it for identification, defined in the EXCHFORM.H header file.</span></span> <span data-ttu-id="352b2-107">A tabela a seguir lista os verbos formulário padrão e suas constantes associados:</span><span class="sxs-lookup"><span data-stu-id="352b2-107">The following table lists the standard form verbs and their associated constants:</span></span>
  
|<span data-ttu-id="352b2-108">**Verbo**</span><span class="sxs-lookup"><span data-stu-id="352b2-108">**Verb**</span></span>|<span data-ttu-id="352b2-109">**Valor**</span><span class="sxs-lookup"><span data-stu-id="352b2-109">**Value**</span></span>|
|:-----|:-----|
|<span data-ttu-id="352b2-110">Abrir</span><span class="sxs-lookup"><span data-stu-id="352b2-110">Open</span></span>  <br/> |<span data-ttu-id="352b2-111">EXCHIVERB_OPEN</span><span class="sxs-lookup"><span data-stu-id="352b2-111">EXCHIVERB_OPEN</span></span>  <br/> |
|<span data-ttu-id="352b2-112">Responder</span><span class="sxs-lookup"><span data-stu-id="352b2-112">Reply</span></span>  <br/> |<span data-ttu-id="352b2-113">EXCHIVERB_REPLYTOSENDER</span><span class="sxs-lookup"><span data-stu-id="352b2-113">EXCHIVERB_REPLYTOSENDER</span></span>  <br/> |
|<span data-ttu-id="352b2-114">Responder a Todos</span><span class="sxs-lookup"><span data-stu-id="352b2-114">Reply to All</span></span>  <br/> |<span data-ttu-id="352b2-115">EXCHIVERB_REPLYTOALL</span><span class="sxs-lookup"><span data-stu-id="352b2-115">EXCHIVERB_REPLYTOALL</span></span>  <br/> |
|<span data-ttu-id="352b2-116">Encaminhar</span><span class="sxs-lookup"><span data-stu-id="352b2-116">Forward</span></span>  <br/> |<span data-ttu-id="352b2-117">EXCHIVERB_FORWARD</span><span class="sxs-lookup"><span data-stu-id="352b2-117">EXCHIVERB_FORWARD</span></span>  <br/> |
|<span data-ttu-id="352b2-118">Imprimir</span><span class="sxs-lookup"><span data-stu-id="352b2-118">Print</span></span>  <br/> |<span data-ttu-id="352b2-119">EXCHIVERB_PRINT</span><span class="sxs-lookup"><span data-stu-id="352b2-119">EXCHIVERB_PRINT</span></span>  <br/> |
|<span data-ttu-id="352b2-120">Salvar como</span><span class="sxs-lookup"><span data-stu-id="352b2-120">Save As</span></span>  <br/> |<span data-ttu-id="352b2-121">EXCHIVERB_SAVEAS</span><span class="sxs-lookup"><span data-stu-id="352b2-121">EXCHIVERB_SAVEAS</span></span>  <br/> |
|<span data-ttu-id="352b2-122">Responder para Pasta</span><span class="sxs-lookup"><span data-stu-id="352b2-122">Reply to Folder</span></span>  <br/> |<span data-ttu-id="352b2-123">EXCHIVERB_REPLYTOFOLDER</span><span class="sxs-lookup"><span data-stu-id="352b2-123">EXCHIVERB_REPLYTOFOLDER</span></span>  <br/> |
   
<span data-ttu-id="352b2-124">Quando o usuário escolhe um verbo, passe sua constante em uma chamada ao método de [IMAPIForm::DoVerb](imapiform-doverb.md) do formulário para executar sua ação correspondente.</span><span class="sxs-lookup"><span data-stu-id="352b2-124">When a user chooses a verb, pass its constant in a call to the form's [IMAPIForm::DoVerb](imapiform-doverb.md) method to perform its corresponding action.</span></span> 
  
<span data-ttu-id="352b2-125">Além das acessando verbos através de sua tela de formulário, às vezes, os usuários podem acessar o verbos diretamente do formulário.</span><span class="sxs-lookup"><span data-stu-id="352b2-125">In addition to accessing verbs through your form viewer, users can sometimes access verbs directly from the form.</span></span> <span data-ttu-id="352b2-126">Por exemplo, alguns objetos de formulário permitem que o usuário invocar o verbo **Imprimir** clicando duas vezes no formulário e escolhendo a **impressão** de um menu sensível ao contexto.</span><span class="sxs-lookup"><span data-stu-id="352b2-126">For example, some form objects allow the user to invoke the **Print** verb by right-clicking on the form and choosing **Print** from a context-sensitive menu.</span></span> 
  

