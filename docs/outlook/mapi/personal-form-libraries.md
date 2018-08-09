---
title: Bibliotecas de formulários pessoais
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 6ffcd93c-3737-4342-9cd0-2ca7c0fba52c
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 0793fefd744eecc95899c4166cb8a1a6a2e6cd2f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19768212"
---
# <a name="personal-form-libraries"></a><span data-ttu-id="f5176-103">Bibliotecas de formulários pessoais</span><span class="sxs-lookup"><span data-stu-id="f5176-103">Personal Form Libraries</span></span>

  
  
<span data-ttu-id="f5176-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="f5176-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="f5176-105">Como seu nome sugere, bibliotecas de formulários particulares contêm formulários de interesse para um usuário específico.</span><span class="sxs-lookup"><span data-stu-id="f5176-105">As its name suggests, personal form libraries contain forms of interest to a particular user.</span></span> <span data-ttu-id="f5176-106">Biblioteca de formulários particular do usuário é a biblioteca de formulários associada ao repositório de mensagem padrão identificado no perfil do usuário; cada perfil instalado em uma estação de trabalho pode usar um repositório separado padrão e, portanto, uma biblioteca de formulários particulares separado.</span><span class="sxs-lookup"><span data-stu-id="f5176-106">A user's personal form library is the form library associated with the default message store identified in the user's profile; each profile installed on a workstation can use a separate default store, and therefore, a separate personal form library.</span></span> <span data-ttu-id="f5176-107">Uma biblioteca de formulários particulares pode conter cópias das formas que também estão contidas em outras bibliotecas de formulários, além de outras formas.</span><span class="sxs-lookup"><span data-stu-id="f5176-107">A personal form library can contain copies of forms that are also contained in other form libraries in addition to other forms.</span></span>
  
<span data-ttu-id="f5176-108">Uma biblioteca de formulários particular é implementada na tabela de conteúdo associados da pasta raiz no armazenamento de mensagens do usuário padrão — se que reside em um servidor ou localmente na estação de trabalho do usuário é irrelevante.</span><span class="sxs-lookup"><span data-stu-id="f5176-108">A personal form library is implemented in the associated-contents table of the root folder in a user's default message store — whether that resides on a server or locally on the user's workstation is immaterial.</span></span> <span data-ttu-id="f5176-109">Se o armazenamento de mensagens padrão do usuário é armazenado na estação de trabalho do usuário, bibliotecas de formulários particulares oferecem desempenho aprimorado, permitindo que aplicativos acessem os formulários localmente, em vez de pela rede.</span><span class="sxs-lookup"><span data-stu-id="f5176-109">If the user's default message store is stored on the user's workstation, personal form libraries offer enhanced performance by enabling applications to access forms locally instead of over the network.</span></span> <span data-ttu-id="f5176-110">Ele também disponibiliza formulários para usuários trabalhando offline, que podem ocorrer quando os usuários desejam assumir suas formas com eles em computadores portáteis e são sem acesso a uma rede.</span><span class="sxs-lookup"><span data-stu-id="f5176-110">It also makes forms available to users working offline, which can occur when users want to take their forms with them on portable computers and are without access to a network.</span></span>
  
<span data-ttu-id="f5176-111">As propriedades e implementação subjacente de entradas de biblioteca de formulários particulares incluem uma propriedade de "Contêiner ID" que identifica um contêiner de mestre que a entrada de local deve ser sincronizada com.</span><span class="sxs-lookup"><span data-stu-id="f5176-111">The properties and underlying implementation of personal form library entries include a "Container ID" property that identifies a master container that the local entry must be synchronized with.</span></span> <span data-ttu-id="f5176-112">Isso pode ser o identificador de uma pasta arbitrária que contém formulários.</span><span class="sxs-lookup"><span data-stu-id="f5176-112">This can be the identifier of an arbitrary folder that contains forms.</span></span> <span data-ttu-id="f5176-113">Isso é útil se você estiver usando um gerente de formulário personalizado que ofereça suporte a algum tipo de biblioteca de formulários de toda a organização; o gerente do formulário seria cuidam da sincronização de formulários armazenados na biblioteca de formulários particulares e a biblioteca de formulários de toda a organização.</span><span class="sxs-lookup"><span data-stu-id="f5176-113">This is useful if you are using a custom form manager that supports some sort of organization-wide form library; the form manager would take care of synchronizing the forms stored in the personal form library and the organization-wide form library.</span></span> <span data-ttu-id="f5176-114">Isso provavelmente ocorrerá quando o Gerenciador de formulário foi carregado, mas pode acontecer teoricamente a qualquer momento.</span><span class="sxs-lookup"><span data-stu-id="f5176-114">This would probably happen when the form manager was loaded, but could theoretically happen at any time.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="f5176-115">Confira também</span><span class="sxs-lookup"><span data-stu-id="f5176-115">See also</span></span>



[<span data-ttu-id="f5176-116">Formulários MAPI</span><span class="sxs-lookup"><span data-stu-id="f5176-116">MAPI Forms</span></span>](mapi-forms.md)

