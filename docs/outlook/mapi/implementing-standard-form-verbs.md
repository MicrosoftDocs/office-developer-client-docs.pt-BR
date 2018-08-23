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
ms.openlocfilehash: 46585859e1dde4ecf38262f99cac5e3a9d29e5db
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22568746"
---
# <a name="implementing-standard-form-verbs"></a><span data-ttu-id="1fd0e-103">Implementar verbos de formulário padrão</span><span class="sxs-lookup"><span data-stu-id="1fd0e-103">Implementing Standard Form Verbs</span></span>

  
  
<span data-ttu-id="1fd0e-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1fd0e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1fd0e-105">MAPI define um conjunto de verbos padrão ou ações tomadas quando um usuário faz uma seleção de menu ou clicar em um botão, que devem oferecer suporte a todos os visualizadores de formulário.</span><span class="sxs-lookup"><span data-stu-id="1fd0e-105">MAPI defines a set of standard verbs, or actions taken when a user makes a menu selection or clicks a button, that all form viewers should support.</span></span> <span data-ttu-id="1fd0e-106">Cada verbo tem uma constante associada a ela para identificação, definida no EXCHFORM. Arquivo de cabeçalho H.</span><span class="sxs-lookup"><span data-stu-id="1fd0e-106">Each verb has a constant associated with it for identification, defined in the EXCHFORM.H header file.</span></span> <span data-ttu-id="1fd0e-107">A tabela a seguir lista os verbos formulário padrão e suas constantes associados:</span><span class="sxs-lookup"><span data-stu-id="1fd0e-107">The following table lists the standard form verbs and their associated constants:</span></span>
  
|<span data-ttu-id="1fd0e-108">**Verbo**</span><span class="sxs-lookup"><span data-stu-id="1fd0e-108">**Verb**</span></span>|<span data-ttu-id="1fd0e-109">**Valor**</span><span class="sxs-lookup"><span data-stu-id="1fd0e-109">**Value**</span></span>|
|:-----|:-----|
|<span data-ttu-id="1fd0e-110">Abrir</span><span class="sxs-lookup"><span data-stu-id="1fd0e-110">Open</span></span>  <br/> |<span data-ttu-id="1fd0e-111">EXCHIVERB_OPEN</span><span class="sxs-lookup"><span data-stu-id="1fd0e-111">EXCHIVERB_OPEN</span></span>  <br/> |
|<span data-ttu-id="1fd0e-112">Responder</span><span class="sxs-lookup"><span data-stu-id="1fd0e-112">Reply</span></span>  <br/> |<span data-ttu-id="1fd0e-113">EXCHIVERB_REPLYTOSENDER</span><span class="sxs-lookup"><span data-stu-id="1fd0e-113">EXCHIVERB_REPLYTOSENDER</span></span>  <br/> |
|<span data-ttu-id="1fd0e-114">Responder a Todos</span><span class="sxs-lookup"><span data-stu-id="1fd0e-114">Reply to All</span></span>  <br/> |<span data-ttu-id="1fd0e-115">EXCHIVERB_REPLYTOALL</span><span class="sxs-lookup"><span data-stu-id="1fd0e-115">EXCHIVERB_REPLYTOALL</span></span>  <br/> |
|<span data-ttu-id="1fd0e-116">Encaminhar</span><span class="sxs-lookup"><span data-stu-id="1fd0e-116">Forward</span></span>  <br/> |<span data-ttu-id="1fd0e-117">EXCHIVERB_FORWARD</span><span class="sxs-lookup"><span data-stu-id="1fd0e-117">EXCHIVERB_FORWARD</span></span>  <br/> |
|<span data-ttu-id="1fd0e-118">Imprimir</span><span class="sxs-lookup"><span data-stu-id="1fd0e-118">Print</span></span>  <br/> |<span data-ttu-id="1fd0e-119">EXCHIVERB_PRINT</span><span class="sxs-lookup"><span data-stu-id="1fd0e-119">EXCHIVERB_PRINT</span></span>  <br/> |
|<span data-ttu-id="1fd0e-120">Salvar como</span><span class="sxs-lookup"><span data-stu-id="1fd0e-120">Save As</span></span>  <br/> |<span data-ttu-id="1fd0e-121">EXCHIVERB_SAVEAS</span><span class="sxs-lookup"><span data-stu-id="1fd0e-121">EXCHIVERB_SAVEAS</span></span>  <br/> |
|<span data-ttu-id="1fd0e-122">Responder para Pasta</span><span class="sxs-lookup"><span data-stu-id="1fd0e-122">Reply to Folder</span></span>  <br/> |<span data-ttu-id="1fd0e-123">EXCHIVERB_REPLYTOFOLDER</span><span class="sxs-lookup"><span data-stu-id="1fd0e-123">EXCHIVERB_REPLYTOFOLDER</span></span>  <br/> |
   
<span data-ttu-id="1fd0e-124">Quando o usuário escolhe um verbo, passe sua constante em uma chamada ao método de [IMAPIForm::DoVerb](imapiform-doverb.md) do formulário para executar sua ação correspondente.</span><span class="sxs-lookup"><span data-stu-id="1fd0e-124">When a user chooses a verb, pass its constant in a call to the form's [IMAPIForm::DoVerb](imapiform-doverb.md) method to perform its corresponding action.</span></span> 
  
<span data-ttu-id="1fd0e-125">Além das acessando verbos através de sua tela de formulário, às vezes, os usuários podem acessar o verbos diretamente do formulário.</span><span class="sxs-lookup"><span data-stu-id="1fd0e-125">In addition to accessing verbs through your form viewer, users can sometimes access verbs directly from the form.</span></span> <span data-ttu-id="1fd0e-126">Por exemplo, alguns objetos de formulário permitem que o usuário invocar o verbo **Imprimir** clicando duas vezes no formulário e escolhendo a **impressão** de um menu sensível ao contexto.</span><span class="sxs-lookup"><span data-stu-id="1fd0e-126">For example, some form objects allow the user to invoke the **Print** verb by right-clicking on the form and choosing **Print** from a context-sensitive menu.</span></span> 
  

