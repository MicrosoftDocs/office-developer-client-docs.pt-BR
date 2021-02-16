---
title: Recursos não suportados por gerentes de formulário
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: b51e9e03-a333-4fdc-b6fe-87bd4e947b9f
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: e31eacaae54968fbdbd9fe0345130a8d09c3509f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419377"
---
# <a name="capabilities-not-supported-by-form-managers"></a><span data-ttu-id="8fdac-103">Recursos não suportados por gerentes de formulário</span><span class="sxs-lookup"><span data-stu-id="8fdac-103">Capabilities Not Supported by Form Managers</span></span>

  
  
<span data-ttu-id="8fdac-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8fdac-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8fdac-105">Os seguintes recursos não são suportados pelo gerenciador de formulário padrão por motivos de desempenho, mas podem ser suportados por gerentes de formulário personalizados.</span><span class="sxs-lookup"><span data-stu-id="8fdac-105">The following features are not supported by the default form manager for performance reasons but can be supported by custom form managers.</span></span>
  
- <span data-ttu-id="8fdac-106">Uma hierarquia que permite que formulários sejam agrupados ou categorizados em uma biblioteca de formulários.</span><span class="sxs-lookup"><span data-stu-id="8fdac-106">A hierarchy that enables forms to be grouped or categorized throughout a form library.</span></span> <span data-ttu-id="8fdac-107">Uma biblioteca de formulários é um banco de dados de arquivos simples de formulários.</span><span class="sxs-lookup"><span data-stu-id="8fdac-107">A form library is a flat-file database of forms.</span></span>
    
- <span data-ttu-id="8fdac-108">Controle de acesso para categorias de formulários, correspondente a classes de mensagens ou superclasses.</span><span class="sxs-lookup"><span data-stu-id="8fdac-108">Access control for categories of forms, corresponding to message classes or superclasses.</span></span>
    
- <span data-ttu-id="8fdac-109">Suporte para várias versões de idioma do mesmo formulário em uma única biblioteca de formulário.</span><span class="sxs-lookup"><span data-stu-id="8fdac-109">Support for multiple language versions of the same form in a single form library.</span></span>
    
<span data-ttu-id="8fdac-110">Esses são os problemas de implementação.</span><span class="sxs-lookup"><span data-stu-id="8fdac-110">These are implementation issues.</span></span> <span data-ttu-id="8fdac-111">Não há nada para impedir que um gerenciador de formulário personalizado implemente esses recursos.</span><span class="sxs-lookup"><span data-stu-id="8fdac-111">There is nothing to prevent a custom form manager from implementing these features.</span></span>
  
<span data-ttu-id="8fdac-112">A arquitetura de formulário MAPI não dá suporte a vários gerentes de formulário sendo executados simultaneamente.</span><span class="sxs-lookup"><span data-stu-id="8fdac-112">The MAPI form architecture does not support multiple form managers running concurrently.</span></span> <span data-ttu-id="8fdac-113">Embora o MAPI seja compatível com vários provedores simultâneos de armazenamento de mensagens, provedores de transporte e de agendas de endereços, apenas um único gerenciador de formulário é suportado.</span><span class="sxs-lookup"><span data-stu-id="8fdac-113">Although MAPI supports multiple concurrent message store providers, transport providers, and address book providers, only a single form manager is supported.</span></span>
  
<span data-ttu-id="8fdac-114">Because only one form manager may be running at once, if you implement a custom form manager you will have to re-implement any functionality from the default form manager that you need.</span><span class="sxs-lookup"><span data-stu-id="8fdac-114">Because only one form manager may be running at once, if you implement a custom form manager you will have to re-implement any functionality from the default form manager that you need.</span></span> <span data-ttu-id="8fdac-115">Como o gerenciador de formulário personalizado substituirá totalmente o gerenciador de formulário padrão, os recursos do gerenciador de formulário padrão estarão indisponíveis, a menos que sejam duplicados no gerenciador de formulário personalizado.</span><span class="sxs-lookup"><span data-stu-id="8fdac-115">Because your custom form manager will entirely replace the default form manager, capabilities of the default form manager will be unavailable unless they are duplicated in your custom form manager.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="8fdac-116">Confira também</span><span class="sxs-lookup"><span data-stu-id="8fdac-116">See also</span></span>



[<span data-ttu-id="8fdac-117">Formulários MAPI</span><span class="sxs-lookup"><span data-stu-id="8fdac-117">MAPI Forms</span></span>](mapi-forms.md)

