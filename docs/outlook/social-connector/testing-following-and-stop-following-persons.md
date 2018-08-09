---
title: Testar o recurso de seguir e deixar de seguir pessoas
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: c603c3c6-62c8-4895-93e1-b2e146dfaa4f
description: Este tópico descreve os cenários para testar a capacidade do provedor do Outlook Social Connector (OSC) a seguir um amigo e pare seguindo um amigo na rede social.
ms.openlocfilehash: 09652b658a2c20301b8b0568d373ae6fe841fe2b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770947"
---
# <a name="testing-following-and-stop-following-persons"></a>Testar o recurso de seguir e deixar de seguir pessoas

Este tópico descreve os cenários para testar a capacidade do provedor do Outlook Social Connector (OSC) a seguir um amigo e pare seguindo um amigo na rede social.
  
## <a name="following-a-person"></a>Seguir uma pessoa

Para seguir uma pessoa é para adicionar uma pessoa como um amigo na rede social, usando o endereço SMTP fornecido pelo item selecionado do Outlook. Seguir alguém em uma rede social geralmente envolve a solicitação de permissão dessa pessoa por um email para o endereço SMTP. Para conceder permissão, essa pessoa deve tanto que já incluído na sua conta de rede social o endereço SMTP ou ser disposto a adicionar esse SMTP para uma conta de rede social. Teste cada um dos seguintes cenários para verificar se o seu provedor OSC se comporta corretamente.
  
|**Cenário**|**Comportamento esperado**|
|:-----|:-----|
|Tentando siga uma pessoa na rede social que existe na rede social.  <br/> |Para uma rede social que não exige a permissão da pessoa, a rede social imediatamente adiciona a pessoa como um amigo.  <br/> Para uma rede que exige permissão dessa pessoa, a rede social envia uma notificação. O painel de pessoas do Outlook exibe um ícone pendente dessa pessoa.  <br/> |
|Tentando siga uma pessoa na rede social que não existir na rede social.  <br/> |O provedor do OSC exibe o erro apropriado no [ISocialSession::FollowPerson](isocialsession-followperson.md) ou [ISocialSession2::FollowPersonEx](isocialsession2-followpersonex.md).  <br/> |
|Seguindo um amigo na rede social.  <br/> |Para o amigo selecionado no painel de pessoas, emblema da rede social e imagens de perfil do amigo para essa rede social são exibidas.  <br/> |
|Selecionando o link para a página de perfil de um amigo.  <br/> |Página do amigo na rede social é aberto no navegador de padrão do usuário conectado.  <br/> |
   
## <a name="stop-following-a-person"></a>Parar a seguir uma pessoa

Para interromper a seguir uma pessoa é remover essa pessoa como um amigo na rede social. Teste o cenário a seguir para verificar as paradas de provedor do OSC seguir uma pessoa adequadamente.
  
|**Cenário**|**Comportamento esperado**|
|:-----|:-----|
|Tentar remover uma pessoa como um amigo na rede social.  <br/> |A rede social não são mais lista essa pessoa como um amigo na conta do usuário conectado.  <br/> |
   
## <a name="see-also"></a>Confira também

- [Preparando-se para o lançamento de um provedor OSC](getting-ready-to-release-an-osc-provider.md)

