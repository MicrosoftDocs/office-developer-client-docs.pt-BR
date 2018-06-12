---
title: Recursos não suportados pelos gerentes de formulário
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: b51e9e03-a333-4fdc-b6fe-87bd4e947b9f
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 86c91353b620482ca0862aa998aae1b3329cfc94
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766240"
---
# <a name="capabilities-not-supported-by-form-managers"></a><span data-ttu-id="61edc-103">Recursos não suportados pelos gerentes de formulário</span><span class="sxs-lookup"><span data-stu-id="61edc-103">Capabilities Not Supported by Form Managers</span></span>

  
  
<span data-ttu-id="61edc-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="61edc-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="61edc-105">Os seguintes recursos não são suportados pelo gerente de formulário padrão por motivos de desempenho, mas podem ser suportados pelos gerentes de formulário personalizado.</span><span class="sxs-lookup"><span data-stu-id="61edc-105">The following features are not supported by the default form manager for performance reasons but can be supported by custom form managers.</span></span>
  
- <span data-ttu-id="61edc-106">Uma hierarquia que permite que os formulários a serem agrupadas ou categorizados em toda uma biblioteca de formulários.</span><span class="sxs-lookup"><span data-stu-id="61edc-106">A hierarchy that enables forms to be grouped or categorized throughout a form library.</span></span> <span data-ttu-id="61edc-107">Uma biblioteca de formulários é um banco de dados de arquivo simples de formulários.</span><span class="sxs-lookup"><span data-stu-id="61edc-107">A form library is a flat-file database of forms.</span></span>
    
- <span data-ttu-id="61edc-108">Controle de acesso para categorias de formulários, correspondente às classes de mensagem ou superclasse.</span><span class="sxs-lookup"><span data-stu-id="61edc-108">Access control for categories of forms, corresponding to message classes or superclasses.</span></span>
    
- <span data-ttu-id="61edc-109">Suporte para várias versões de idioma do mesmo formulário em uma biblioteca de formulário simples.</span><span class="sxs-lookup"><span data-stu-id="61edc-109">Support for multiple language versions of the same form in a single form library.</span></span>
    
<span data-ttu-id="61edc-110">Esses são os problemas de implementação.</span><span class="sxs-lookup"><span data-stu-id="61edc-110">These are implementation issues.</span></span> <span data-ttu-id="61edc-111">Não há nada para impedir que um gerente de formulário personalizado com a implementação desses recursos.</span><span class="sxs-lookup"><span data-stu-id="61edc-111">There is nothing to prevent a custom form manager from implementing these features.</span></span>
  
<span data-ttu-id="61edc-112">A arquitetura de formulário MAPI não oferece suporte a vários gerentes de formulário executando simultaneamente.</span><span class="sxs-lookup"><span data-stu-id="61edc-112">The MAPI form architecture does not support multiple form managers running concurrently.</span></span> <span data-ttu-id="61edc-113">Embora MAPI ofereça suporte a vários provedores de armazenamento de mensagem simultâneas, provedores de transporte e provedores de catálogo de endereços, somente um Gerenciador de formulário simples é suportado.</span><span class="sxs-lookup"><span data-stu-id="61edc-113">Although MAPI supports multiple concurrent message store providers, transport providers, and address book providers, only a single form manager is supported.</span></span>
  
<span data-ttu-id="61edc-114">Porque o Gerenciador de apenas um formulário pode estar em execução ao mesmo tempo, se você implementar um gerente de formulário personalizado, você terá a reimplementação qualquer funcionalidade do Gerenciador de formulário padrão que você precisa.</span><span class="sxs-lookup"><span data-stu-id="61edc-114">Because only one form manager may be running at once, if you implement a custom form manager you will have to re-implement any functionality from the default form manager that you need.</span></span> <span data-ttu-id="61edc-115">Porque seu gerente de formulário personalizado inteiramente substituirá o Gerenciador de formulário padrão, os recursos do Gerenciador de formulário padrão só estará disponíveis a menos que eles são duplicados em seu gerente de formulário personalizado.</span><span class="sxs-lookup"><span data-stu-id="61edc-115">Because your custom form manager will entirely replace the default form manager, capabilities of the default form manager will be unavailable unless they are duplicated in your custom form manager.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="61edc-116">Confira também</span><span class="sxs-lookup"><span data-stu-id="61edc-116">See also</span></span>



[<span data-ttu-id="61edc-117">Formulários MAPI</span><span class="sxs-lookup"><span data-stu-id="61edc-117">MAPI Forms</span></span>](mapi-forms.md)

