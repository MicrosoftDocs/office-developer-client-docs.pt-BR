---
title: Implementando verbos de formulário padrão
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: f89f7c58-6358-4523-9788-676f189b5e69
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 6360b86dc23a5404b818f76cb1c2cd10747ef3cb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426118"
---
# <a name="implementing-standard-form-verbs"></a><span data-ttu-id="6dc07-103">Implementando verbos de formulário padrão</span><span class="sxs-lookup"><span data-stu-id="6dc07-103">Implementing Standard Form Verbs</span></span>

  
  
<span data-ttu-id="6dc07-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6dc07-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6dc07-105">MAPI define um conjunto de verbos padrão, ou ações tomadas quando um usuário faz uma seleção de menu ou clica em um botão, que todos os visualizadores de formulário devem suportar.</span><span class="sxs-lookup"><span data-stu-id="6dc07-105">MAPI defines a set of standard verbs, or actions taken when a user makes a menu selection or clicks a button, that all form viewers should support.</span></span> <span data-ttu-id="6dc07-106">Cada verbo tem uma constante associada a ele para identificação, definida no EXCHFORM. Arquivo de header H.</span><span class="sxs-lookup"><span data-stu-id="6dc07-106">Each verb has a constant associated with it for identification, defined in the EXCHFORM.H header file.</span></span> <span data-ttu-id="6dc07-107">A tabela a seguir lista os verbos de formulário padrão e suas constantes associadas:</span><span class="sxs-lookup"><span data-stu-id="6dc07-107">The following table lists the standard form verbs and their associated constants:</span></span>
  
|<span data-ttu-id="6dc07-108">**Verb**</span><span class="sxs-lookup"><span data-stu-id="6dc07-108">**Verb**</span></span>|<span data-ttu-id="6dc07-109">**Valor**</span><span class="sxs-lookup"><span data-stu-id="6dc07-109">**Value**</span></span>|
|:-----|:-----|
|<span data-ttu-id="6dc07-110">Abrir</span><span class="sxs-lookup"><span data-stu-id="6dc07-110">Open</span></span>  <br/> |<span data-ttu-id="6dc07-111">EXCHIVERB_OPEN</span><span class="sxs-lookup"><span data-stu-id="6dc07-111">EXCHIVERB_OPEN</span></span>  <br/> |
|<span data-ttu-id="6dc07-112">Responder</span><span class="sxs-lookup"><span data-stu-id="6dc07-112">Reply</span></span>  <br/> |<span data-ttu-id="6dc07-113">EXCHIVERB_REPLYTOSENDER</span><span class="sxs-lookup"><span data-stu-id="6dc07-113">EXCHIVERB_REPLYTOSENDER</span></span>  <br/> |
|<span data-ttu-id="6dc07-114">Responder a Todos</span><span class="sxs-lookup"><span data-stu-id="6dc07-114">Reply to All</span></span>  <br/> |<span data-ttu-id="6dc07-115">EXCHIVERB_REPLYTOALL</span><span class="sxs-lookup"><span data-stu-id="6dc07-115">EXCHIVERB_REPLYTOALL</span></span>  <br/> |
|<span data-ttu-id="6dc07-116">Encaminhar</span><span class="sxs-lookup"><span data-stu-id="6dc07-116">Forward</span></span>  <br/> |<span data-ttu-id="6dc07-117">EXCHIVERB_FORWARD</span><span class="sxs-lookup"><span data-stu-id="6dc07-117">EXCHIVERB_FORWARD</span></span>  <br/> |
|<span data-ttu-id="6dc07-118">Imprimir</span><span class="sxs-lookup"><span data-stu-id="6dc07-118">Print</span></span>  <br/> |<span data-ttu-id="6dc07-119">EXCHIVERB_PRINT</span><span class="sxs-lookup"><span data-stu-id="6dc07-119">EXCHIVERB_PRINT</span></span>  <br/> |
|<span data-ttu-id="6dc07-120">Salvar como</span><span class="sxs-lookup"><span data-stu-id="6dc07-120">Save As</span></span>  <br/> |<span data-ttu-id="6dc07-121">EXCHIVERB_SAVEAS</span><span class="sxs-lookup"><span data-stu-id="6dc07-121">EXCHIVERB_SAVEAS</span></span>  <br/> |
|<span data-ttu-id="6dc07-122">Responder para Pasta</span><span class="sxs-lookup"><span data-stu-id="6dc07-122">Reply to Folder</span></span>  <br/> |<span data-ttu-id="6dc07-123">EXCHIVERB_REPLYTOFOLDER</span><span class="sxs-lookup"><span data-stu-id="6dc07-123">EXCHIVERB_REPLYTOFOLDER</span></span>  <br/> |
   
<span data-ttu-id="6dc07-124">Quando um usuário escolher um verbo, passe sua constante em uma chamada para o método [IMAPIForm::D oVerb](imapiform-doverb.md) do formulário para executar sua ação correspondente.</span><span class="sxs-lookup"><span data-stu-id="6dc07-124">When a user chooses a verb, pass its constant in a call to the form's [IMAPIForm::DoVerb](imapiform-doverb.md) method to perform its corresponding action.</span></span> 
  
<span data-ttu-id="6dc07-125">Além de acessar verbos por meio do visualizador de formulário, os usuários podem, às vezes, acessar verbos diretamente do formulário.</span><span class="sxs-lookup"><span data-stu-id="6dc07-125">In addition to accessing verbs through your form viewer, users can sometimes access verbs directly from the form.</span></span> <span data-ttu-id="6dc07-126">For example, some form objects allow the user to invoke the Print verb by **right-clicking** on the form and choosing **Print** from a context-sensitive menu.</span><span class="sxs-lookup"><span data-stu-id="6dc07-126">For example, some form objects allow the user to invoke the **Print** verb by right-clicking on the form and choosing **Print** from a context-sensitive menu.</span></span> 
  

