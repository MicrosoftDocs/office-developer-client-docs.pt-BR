---
title: Bibliotecas de Formulário Pessoal
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 6ffcd93c-3737-4342-9cd0-2ca7c0fba52c
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: c84665077f9c8e02647a4d348042515366b0c090
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420406"
---
# <a name="personal-form-libraries"></a><span data-ttu-id="63763-103">Bibliotecas de Formulário Pessoal</span><span class="sxs-lookup"><span data-stu-id="63763-103">Personal Form Libraries</span></span>

  
  
<span data-ttu-id="63763-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="63763-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="63763-105">Como o nome sugere, as bibliotecas de formulários pessoais contêm formas de interesse para um usuário específico.</span><span class="sxs-lookup"><span data-stu-id="63763-105">As its name suggests, personal form libraries contain forms of interest to a particular user.</span></span> <span data-ttu-id="63763-106">A biblioteca de formulário pessoal de um usuário é a biblioteca de formulário associada ao armazenamento de mensagens padrão identificado no perfil do usuário; cada perfil instalado em uma estação de trabalho pode usar um armazenamento padrão separado e, portanto, uma biblioteca de formulário pessoal separada.</span><span class="sxs-lookup"><span data-stu-id="63763-106">A user's personal form library is the form library associated with the default message store identified in the user's profile; each profile installed on a workstation can use a separate default store, and therefore, a separate personal form library.</span></span> <span data-ttu-id="63763-107">Uma biblioteca de formulários pessoais pode conter cópias de formulários que também estão contidas em outras bibliotecas de formulários, além de outros formulários.</span><span class="sxs-lookup"><span data-stu-id="63763-107">A personal form library can contain copies of forms that are also contained in other form libraries in addition to other forms.</span></span>
  
<span data-ttu-id="63763-108">Uma biblioteca de formulário pessoal é implementada na tabela de conteúdo associado da pasta raiz no armazenamento de mensagens padrão de um usuário — independentemente de residir em um servidor ou localmente na estação de trabalho do usuário seja imaterial.</span><span class="sxs-lookup"><span data-stu-id="63763-108">A personal form library is implemented in the associated-contents table of the root folder in a user's default message store — whether that resides on a server or locally on the user's workstation is immaterial.</span></span> <span data-ttu-id="63763-109">Se o armazenamento de mensagens padrão do usuário estiver armazenado na estação de trabalho do usuário, as bibliotecas de formulários pessoais oferecerão um desempenho aprimorado, permitindo que os aplicativos acessem formulários localmente em vez de pela rede.</span><span class="sxs-lookup"><span data-stu-id="63763-109">If the user's default message store is stored on the user's workstation, personal form libraries offer enhanced performance by enabling applications to access forms locally instead of over the network.</span></span> <span data-ttu-id="63763-110">Ele também disponibiliza formulários para usuários que trabalham offline, o que pode ocorrer quando os usuários querem tirar seus formulários com eles em computadores portáteis e não têm acesso a uma rede.</span><span class="sxs-lookup"><span data-stu-id="63763-110">It also makes forms available to users working offline, which can occur when users want to take their forms with them on portable computers and are without access to a network.</span></span>
  
<span data-ttu-id="63763-111">As propriedades e a implementação subjacente de entradas da biblioteca de formulário pessoal incluem uma propriedade "ID do contêiner" que identifica um contêiner mestre com o que a entrada local deve ser sincronizada.</span><span class="sxs-lookup"><span data-stu-id="63763-111">The properties and underlying implementation of personal form library entries include a "Container ID" property that identifies a master container that the local entry must be synchronized with.</span></span> <span data-ttu-id="63763-112">Pode ser o identificador de uma pasta arbitrária que contém formulários.</span><span class="sxs-lookup"><span data-stu-id="63763-112">This can be the identifier of an arbitrary folder that contains forms.</span></span> <span data-ttu-id="63763-113">Isso será útil se você estiver usando um gerenciador de formulário personalizado que oferece suporte a algum tipo de biblioteca de formulário em toda a organização; o gerenciador de formulários cuidaria da sincronização dos formulários armazenados na biblioteca de formulários pessoais e na biblioteca de formulários de toda a organização.</span><span class="sxs-lookup"><span data-stu-id="63763-113">This is useful if you are using a custom form manager that supports some sort of organization-wide form library; the form manager would take care of synchronizing the forms stored in the personal form library and the organization-wide form library.</span></span> <span data-ttu-id="63763-114">Isso provavelmente ocorreria quando o gerenciador de formulário fosse carregado, mas teoricamente poderia acontecer a qualquer momento.</span><span class="sxs-lookup"><span data-stu-id="63763-114">This would probably happen when the form manager was loaded, but could theoretically happen at any time.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="63763-115">Confira também</span><span class="sxs-lookup"><span data-stu-id="63763-115">See also</span></span>



[<span data-ttu-id="63763-116">Formulários MAPI</span><span class="sxs-lookup"><span data-stu-id="63763-116">MAPI Forms</span></span>](mapi-forms.md)

