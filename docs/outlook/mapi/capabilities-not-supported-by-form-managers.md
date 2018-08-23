---
title: Recursos incompatíveis com gerentes de formulário
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: b51e9e03-a333-4fdc-b6fe-87bd4e947b9f
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: a84c0a93f80080b71f6049e73f0a0094c38c28ef
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22566870"
---
# <a name="capabilities-not-supported-by-form-managers"></a><span data-ttu-id="7af62-103">Recursos incompatíveis com gerentes de formulário</span><span class="sxs-lookup"><span data-stu-id="7af62-103">Capabilities Not Supported by Form Managers</span></span>

  
  
<span data-ttu-id="7af62-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7af62-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7af62-105">Os seguintes recursos não são suportados pelo gerente de formulário padrão por motivos de desempenho, mas podem ser suportados pelos gerentes de formulário personalizado.</span><span class="sxs-lookup"><span data-stu-id="7af62-105">The following features are not supported by the default form manager for performance reasons but can be supported by custom form managers.</span></span>
  
- <span data-ttu-id="7af62-106">Uma hierarquia que permite que os formulários a serem agrupadas ou categorizados em toda uma biblioteca de formulários.</span><span class="sxs-lookup"><span data-stu-id="7af62-106">A hierarchy that enables forms to be grouped or categorized throughout a form library.</span></span> <span data-ttu-id="7af62-107">Uma biblioteca de formulários é um banco de dados de arquivo simples de formulários.</span><span class="sxs-lookup"><span data-stu-id="7af62-107">A form library is a flat-file database of forms.</span></span>
    
- <span data-ttu-id="7af62-108">Controle de acesso para categorias de formulários, correspondente às classes de mensagem ou superclasse.</span><span class="sxs-lookup"><span data-stu-id="7af62-108">Access control for categories of forms, corresponding to message classes or superclasses.</span></span>
    
- <span data-ttu-id="7af62-109">Suporte para várias versões de idioma do mesmo formulário em uma biblioteca de formulário simples.</span><span class="sxs-lookup"><span data-stu-id="7af62-109">Support for multiple language versions of the same form in a single form library.</span></span>
    
<span data-ttu-id="7af62-110">Esses são os problemas de implementação.</span><span class="sxs-lookup"><span data-stu-id="7af62-110">These are implementation issues.</span></span> <span data-ttu-id="7af62-111">Não há nada para impedir que um gerente de formulário personalizado com a implementação desses recursos.</span><span class="sxs-lookup"><span data-stu-id="7af62-111">There is nothing to prevent a custom form manager from implementing these features.</span></span>
  
<span data-ttu-id="7af62-112">A arquitetura de formulário MAPI não oferece suporte a vários gerentes de formulário executando simultaneamente.</span><span class="sxs-lookup"><span data-stu-id="7af62-112">The MAPI form architecture does not support multiple form managers running concurrently.</span></span> <span data-ttu-id="7af62-113">Embora MAPI ofereça suporte a vários provedores de armazenamento de mensagem simultâneas, provedores de transporte e provedores de catálogo de endereços, somente um Gerenciador de formulário simples é suportado.</span><span class="sxs-lookup"><span data-stu-id="7af62-113">Although MAPI supports multiple concurrent message store providers, transport providers, and address book providers, only a single form manager is supported.</span></span>
  
<span data-ttu-id="7af62-114">Porque o Gerenciador de apenas um formulário pode estar em execução ao mesmo tempo, se você implementar um gerente de formulário personalizado, você terá a reimplementação qualquer funcionalidade do Gerenciador de formulário padrão que você precisa.</span><span class="sxs-lookup"><span data-stu-id="7af62-114">Because only one form manager may be running at once, if you implement a custom form manager you will have to re-implement any functionality from the default form manager that you need.</span></span> <span data-ttu-id="7af62-115">Porque seu gerente de formulário personalizado inteiramente substituirá o Gerenciador de formulário padrão, os recursos do Gerenciador de formulário padrão só estará disponíveis a menos que eles são duplicados em seu gerente de formulário personalizado.</span><span class="sxs-lookup"><span data-stu-id="7af62-115">Because your custom form manager will entirely replace the default form manager, capabilities of the default form manager will be unavailable unless they are duplicated in your custom form manager.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="7af62-116">Confira também</span><span class="sxs-lookup"><span data-stu-id="7af62-116">See also</span></span>



[<span data-ttu-id="7af62-117">Formulários MAPI</span><span class="sxs-lookup"><span data-stu-id="7af62-117">MAPI Forms</span></span>](mapi-forms.md)

