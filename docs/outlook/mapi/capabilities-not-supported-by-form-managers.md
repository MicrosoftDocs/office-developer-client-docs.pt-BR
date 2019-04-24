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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326373"
---
# <a name="capabilities-not-supported-by-form-managers"></a><span data-ttu-id="f327a-103">Recursos não suportados por gerentes de formulário</span><span class="sxs-lookup"><span data-stu-id="f327a-103">Capabilities Not Supported by Form Managers</span></span>

  
  
<span data-ttu-id="f327a-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f327a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f327a-105">Os recursos a seguir não são suportados pelo Gerenciador de formulários padrão por motivos de desempenho, mas podem ser suportados por gerentes de formulários personalizados.</span><span class="sxs-lookup"><span data-stu-id="f327a-105">The following features are not supported by the default form manager for performance reasons but can be supported by custom form managers.</span></span>
  
- <span data-ttu-id="f327a-106">Uma hierarquia que permite que os formulários sejam agrupados ou categorizados em uma biblioteca de formulários.</span><span class="sxs-lookup"><span data-stu-id="f327a-106">A hierarchy that enables forms to be grouped or categorized throughout a form library.</span></span> <span data-ttu-id="f327a-107">Uma biblioteca de formulários é um banco de dados de arquivo simples de formulários.</span><span class="sxs-lookup"><span data-stu-id="f327a-107">A form library is a flat-file database of forms.</span></span>
    
- <span data-ttu-id="f327a-108">Controle de acesso para categorias de formulários, correspondentes a classes de mensagens ou superclasses.</span><span class="sxs-lookup"><span data-stu-id="f327a-108">Access control for categories of forms, corresponding to message classes or superclasses.</span></span>
    
- <span data-ttu-id="f327a-109">Suporte para versões de vários idiomas do mesmo formulário em uma única biblioteca de formulários.</span><span class="sxs-lookup"><span data-stu-id="f327a-109">Support for multiple language versions of the same form in a single form library.</span></span>
    
<span data-ttu-id="f327a-110">Estes são problemas de implementação.</span><span class="sxs-lookup"><span data-stu-id="f327a-110">These are implementation issues.</span></span> <span data-ttu-id="f327a-111">Não há nada para impedir que um gerente de formulário personalizado implemente esses recursos.</span><span class="sxs-lookup"><span data-stu-id="f327a-111">There is nothing to prevent a custom form manager from implementing these features.</span></span>
  
<span data-ttu-id="f327a-112">A arquitetura de formulário MAPI não dá suporte a vários gerentes de formulários executados simultaneamente.</span><span class="sxs-lookup"><span data-stu-id="f327a-112">The MAPI form architecture does not support multiple form managers running concurrently.</span></span> <span data-ttu-id="f327a-113">Embora o MAPI dê suporte a vários provedores de repositório de mensagens simultâneos, provedores de transporte e provedores de catálogo de endereços, só há suporte para um único Gerenciador de formulários.</span><span class="sxs-lookup"><span data-stu-id="f327a-113">Although MAPI supports multiple concurrent message store providers, transport providers, and address book providers, only a single form manager is supported.</span></span>
  
<span data-ttu-id="f327a-114">Como apenas um gerente de formulário pode ser executado ao mesmo tempo, se você implementar um gerente de formulário personalizado, será necessário reimplementar qualquer funcionalidade do Gerenciador de formulários padrão que você precisa.</span><span class="sxs-lookup"><span data-stu-id="f327a-114">Because only one form manager may be running at once, if you implement a custom form manager you will have to re-implement any functionality from the default form manager that you need.</span></span> <span data-ttu-id="f327a-115">Como o gerente de formulário personalizado substituirá totalmente o Gerenciador de formulários padrão, os recursos do Gerenciador de formulários padrão não estarão disponíveis, a menos que sejam duplicados no seu gerente de formulário personalizado.</span><span class="sxs-lookup"><span data-stu-id="f327a-115">Because your custom form manager will entirely replace the default form manager, capabilities of the default form manager will be unavailable unless they are duplicated in your custom form manager.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="f327a-116">Confira também</span><span class="sxs-lookup"><span data-stu-id="f327a-116">See also</span></span>



[<span data-ttu-id="f327a-117">Formulários MAPI</span><span class="sxs-lookup"><span data-stu-id="f327a-117">MAPI Forms</span></span>](mapi-forms.md)

