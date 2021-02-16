---
title: Testar o recurso de seguir e deixar de seguir pessoas
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: c603c3c6-62c8-4895-93e1-b2e146dfaa4f
description: Este tópico descreve cenários para testar a capacidade do provedor do Outlook Social Connector (OSC) de seguir um amigo e parar de seguir um amigo na rede social.
ms.openlocfilehash: 06a2bc48fa723f4d4513376cace96a195cef9fa3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432447"
---
# <a name="testing-following-and-stop-following-persons"></a><span data-ttu-id="1b75d-103">Testar o recurso de seguir e deixar de seguir pessoas</span><span class="sxs-lookup"><span data-stu-id="1b75d-103">Testing following and stop-following persons</span></span>

<span data-ttu-id="1b75d-104">Este tópico descreve cenários para testar a capacidade do provedor do Outlook Social Connector (OSC) de seguir um amigo e parar de seguir um amigo na rede social.</span><span class="sxs-lookup"><span data-stu-id="1b75d-104">This topic describes scenarios to test the Outlook Social Connector (OSC) provider's ability to follow a friend, and to stop following a friend on the social network.</span></span>
  
## <a name="following-a-person"></a><span data-ttu-id="1b75d-105">Seguir uma pessoa</span><span class="sxs-lookup"><span data-stu-id="1b75d-105">Following a person</span></span>

<span data-ttu-id="1b75d-106">Para seguir uma pessoa é adicionar uma pessoa como um amigo na rede social, usando o endereço SMTP fornecido pelo item selecionado do Outlook.</span><span class="sxs-lookup"><span data-stu-id="1b75d-106">To follow a person is to add a person as a friend on the social network, using the SMTP address provided by the selected Outlook item.</span></span> <span data-ttu-id="1b75d-107">Seguir alguém em uma rede social geralmente envolve a solicitação de permissão dessa pessoa por um email para esse endereço SMTP.</span><span class="sxs-lookup"><span data-stu-id="1b75d-107">Following someone on a social network usually involves requesting permission from that person by an email to that SMTP address.</span></span> <span data-ttu-id="1b75d-108">Para conceder permissão, essa pessoa deve ter esse endereço SMTP já incluído em sua conta de rede social ou estar disposto a adicionar esse SMTP a uma conta de rede social.</span><span class="sxs-lookup"><span data-stu-id="1b75d-108">In order to grant permission, that person must either have that SMTP address already included in his or her social network account, or be willing to add that SMTP to a social network account.</span></span> <span data-ttu-id="1b75d-109">Teste cada um dos seguintes cenários para verificar se o provedor do OSC se comporta corretamente.</span><span class="sxs-lookup"><span data-stu-id="1b75d-109">Test each of the following scenarios to verify that your OSC provider behaves correctly.</span></span>
  
|<span data-ttu-id="1b75d-110">**Cenário**</span><span class="sxs-lookup"><span data-stu-id="1b75d-110">**Scenario**</span></span>|<span data-ttu-id="1b75d-111">**Comportamento esperado**</span><span class="sxs-lookup"><span data-stu-id="1b75d-111">**Expected behavior**</span></span>|
|:-----|:-----|
|<span data-ttu-id="1b75d-112">Tentar seguir uma pessoa na rede social que existe na rede social.</span><span class="sxs-lookup"><span data-stu-id="1b75d-112">Attempting to follow a person on the social network who exists on the social network.</span></span>  <br/> |<span data-ttu-id="1b75d-113">Para uma rede social que não exige permissão da pessoa, a rede social imediatamente adiciona a pessoa como um amigo.</span><span class="sxs-lookup"><span data-stu-id="1b75d-113">For a social network that does not require permission from the person, the social network immediately adds the person as a friend.</span></span>  <br/> <span data-ttu-id="1b75d-114">Para uma rede que exige permissão dessa pessoa, a rede social envia uma notificação.</span><span class="sxs-lookup"><span data-stu-id="1b75d-114">For a network that requires permission from that person, the social network sends a notification.</span></span> <span data-ttu-id="1b75d-115">O Painel de Pessoas do Outlook exibe um ícone pendente para essa pessoa.</span><span class="sxs-lookup"><span data-stu-id="1b75d-115">The Outlook People Pane displays a pending icon for that person.</span></span>  <br/> |
|<span data-ttu-id="1b75d-116">Tentar seguir uma pessoa na rede social que não existe na rede social.</span><span class="sxs-lookup"><span data-stu-id="1b75d-116">Attempting to follow a person on the social network who does not exist on the social network.</span></span>  <br/> |<span data-ttu-id="1b75d-117">O provedor OSC exibe o erro apropriado [em ISocialSession::FollowPerson](isocialsession-followperson.md) ou [ISocialSession2::FollowPersonEx](isocialsession2-followpersonex.md).</span><span class="sxs-lookup"><span data-stu-id="1b75d-117">The OSC provider displays the appropriate error in [ISocialSession::FollowPerson](isocialsession-followperson.md) or [ISocialSession2::FollowPersonEx](isocialsession2-followpersonex.md).</span></span>  <br/> |
|<span data-ttu-id="1b75d-118">Seguindo um amigo na rede social.</span><span class="sxs-lookup"><span data-stu-id="1b75d-118">Following a friend on the social network.</span></span>  <br/> |<span data-ttu-id="1b75d-119">Para o amigo selecionado no Painel de Pessoas, o selo da rede social e a imagem de perfil do amigo dessa rede social são exibidos.</span><span class="sxs-lookup"><span data-stu-id="1b75d-119">For the friend selected in the People Pane, the social network's badge and the friend's profile picture for that social network are displayed.</span></span>  <br/> |
|<span data-ttu-id="1b75d-120">Selecionando o link para a página de perfil de um amigo.</span><span class="sxs-lookup"><span data-stu-id="1b75d-120">Selecting the link to the profile page of a friend.</span></span>  <br/> |<span data-ttu-id="1b75d-121">A página do amigo na rede social é aberta no navegador padrão do usuário conectado.</span><span class="sxs-lookup"><span data-stu-id="1b75d-121">The friend's page on the social network opens in the logged-on user's default browser.</span></span>  <br/> |
   
## <a name="stop-following-a-person"></a><span data-ttu-id="1b75d-122">Parar de seguir uma pessoa</span><span class="sxs-lookup"><span data-stu-id="1b75d-122">Stop following a person</span></span>

<span data-ttu-id="1b75d-123">Para parar de seguir uma pessoa é remover essa pessoa como um amigo na rede social.</span><span class="sxs-lookup"><span data-stu-id="1b75d-123">To stop following a person is to remove that person as a friend on the social network.</span></span> <span data-ttu-id="1b75d-124">Teste o cenário a seguir para verificar se o provedor do OSC para de seguir uma pessoa corretamente.</span><span class="sxs-lookup"><span data-stu-id="1b75d-124">Test the following scenario to verify your OSC provider stops following a person properly.</span></span>
  
|<span data-ttu-id="1b75d-125">**Cenário**</span><span class="sxs-lookup"><span data-stu-id="1b75d-125">**Scenario**</span></span>|<span data-ttu-id="1b75d-126">**Comportamento esperado**</span><span class="sxs-lookup"><span data-stu-id="1b75d-126">**Expected behavior**</span></span>|
|:-----|:-----|
|<span data-ttu-id="1b75d-127">Tentar remover uma pessoa como um amigo na rede social.</span><span class="sxs-lookup"><span data-stu-id="1b75d-127">Attempting to remove a person as a friend on the social network.</span></span>  <br/> |<span data-ttu-id="1b75d-128">A rede social não lista mais essa pessoa como um amigo na conta do usuário conectado.</span><span class="sxs-lookup"><span data-stu-id="1b75d-128">The social network no longer lists that person as a friend on the logged on user's account.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="1b75d-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="1b75d-129">See also</span></span>

- [<span data-ttu-id="1b75d-130">Preparar um provedor de OSC para lançamento</span><span class="sxs-lookup"><span data-stu-id="1b75d-130">Getting Ready to Release an OSC Provider</span></span>](getting-ready-to-release-an-osc-provider.md)

