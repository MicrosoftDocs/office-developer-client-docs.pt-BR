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
ms.openlocfilehash: 6360b86dc23a5404b818f76cb1c2cd10747ef3cb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317441"
---
# <a name="implementing-standard-form-verbs"></a><span data-ttu-id="be32c-103">Implementar verbos de formulário padrão</span><span class="sxs-lookup"><span data-stu-id="be32c-103">Implementing Standard Form Verbs</span></span>

  
  
<span data-ttu-id="be32c-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="be32c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="be32c-105">O MAPI define um conjunto de verbos padrão ou ações executadas quando um usuário faz uma seleção de menu ou clica em um botão, que todos os visualizadores de formulários devem oferecer suporte.</span><span class="sxs-lookup"><span data-stu-id="be32c-105">MAPI defines a set of standard verbs, or actions taken when a user makes a menu selection or clicks a button, that all form viewers should support.</span></span> <span data-ttu-id="be32c-106">Cada verbo tem uma constante associada a ela para identificação, definida no EXCHFORM. Arquivo de cabeçalho H.</span><span class="sxs-lookup"><span data-stu-id="be32c-106">Each verb has a constant associated with it for identification, defined in the EXCHFORM.H header file.</span></span> <span data-ttu-id="be32c-107">A tabela a seguir lista os verbos de formulário padrão e suas constantes associadas:</span><span class="sxs-lookup"><span data-stu-id="be32c-107">The following table lists the standard form verbs and their associated constants:</span></span>
  
|<span data-ttu-id="be32c-108">**Verb**</span><span class="sxs-lookup"><span data-stu-id="be32c-108">**Verb**</span></span>|<span data-ttu-id="be32c-109">**Valor**</span><span class="sxs-lookup"><span data-stu-id="be32c-109">**Value**</span></span>|
|:-----|:-----|
|<span data-ttu-id="be32c-110">Abrir</span><span class="sxs-lookup"><span data-stu-id="be32c-110">Open</span></span>  <br/> |<span data-ttu-id="be32c-111">EXCHIVERB_OPEN</span><span class="sxs-lookup"><span data-stu-id="be32c-111">EXCHIVERB_OPEN</span></span>  <br/> |
|<span data-ttu-id="be32c-112">Responder</span><span class="sxs-lookup"><span data-stu-id="be32c-112">Reply</span></span>  <br/> |<span data-ttu-id="be32c-113">EXCHIVERB_REPLYTOSENDER</span><span class="sxs-lookup"><span data-stu-id="be32c-113">EXCHIVERB_REPLYTOSENDER</span></span>  <br/> |
|<span data-ttu-id="be32c-114">Responder a Todos</span><span class="sxs-lookup"><span data-stu-id="be32c-114">Reply to All</span></span>  <br/> |<span data-ttu-id="be32c-115">EXCHIVERB_REPLYTOALL</span><span class="sxs-lookup"><span data-stu-id="be32c-115">EXCHIVERB_REPLYTOALL</span></span>  <br/> |
|<span data-ttu-id="be32c-116">Encaminhar</span><span class="sxs-lookup"><span data-stu-id="be32c-116">Forward</span></span>  <br/> |<span data-ttu-id="be32c-117">EXCHIVERB_FORWARD</span><span class="sxs-lookup"><span data-stu-id="be32c-117">EXCHIVERB_FORWARD</span></span>  <br/> |
|<span data-ttu-id="be32c-118">Print</span><span class="sxs-lookup"><span data-stu-id="be32c-118">Print</span></span>  <br/> |<span data-ttu-id="be32c-119">EXCHIVERB_PRINT</span><span class="sxs-lookup"><span data-stu-id="be32c-119">EXCHIVERB_PRINT</span></span>  <br/> |
|<span data-ttu-id="be32c-120">Salvar como</span><span class="sxs-lookup"><span data-stu-id="be32c-120">Save As</span></span>  <br/> |<span data-ttu-id="be32c-121">EXCHIVERB_SAVEAS</span><span class="sxs-lookup"><span data-stu-id="be32c-121">EXCHIVERB_SAVEAS</span></span>  <br/> |
|<span data-ttu-id="be32c-122">Responder para Pasta</span><span class="sxs-lookup"><span data-stu-id="be32c-122">Reply to Folder</span></span>  <br/> |<span data-ttu-id="be32c-123">EXCHIVERB_REPLYTOFOLDER</span><span class="sxs-lookup"><span data-stu-id="be32c-123">EXCHIVERB_REPLYTOFOLDER</span></span>  <br/> |
   
<span data-ttu-id="be32c-124">Quando um usuário escolhe um verbo, passe sua constante em uma chamada para o método [IMAPIForm::D overb](imapiform-doverb.md) para executar a ação correspondente.</span><span class="sxs-lookup"><span data-stu-id="be32c-124">When a user chooses a verb, pass its constant in a call to the form's [IMAPIForm::DoVerb](imapiform-doverb.md) method to perform its corresponding action.</span></span> 
  
<span data-ttu-id="be32c-125">Além de acessar verbos por meio de seu visualizador de formulários, os usuários podem, às vezes, acessar verbos diretamente no formulário.</span><span class="sxs-lookup"><span data-stu-id="be32c-125">In addition to accessing verbs through your form viewer, users can sometimes access verbs directly from the form.</span></span> <span data-ttu-id="be32c-126">Por exemplo, alguns objetos Form permitem que o usuário invoque o verbo **Print** clicando com o botão direito do mouse no formulário e escolhendo **Imprimir** de um menu contextual.</span><span class="sxs-lookup"><span data-stu-id="be32c-126">For example, some form objects allow the user to invoke the **Print** verb by right-clicking on the form and choosing **Print** from a context-sensitive menu.</span></span> 
  

