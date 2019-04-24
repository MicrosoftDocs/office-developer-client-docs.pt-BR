---
title: Testar o recurso de seguir e deixar de seguir pessoas
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: c603c3c6-62c8-4895-93e1-b2e146dfaa4f
description: Este tópico descreve cenários para testar a capacidade do provedor do Outlook Social Connector (OSC) de seguir um amigo e para parar de seguir um amigo na rede social.
ms.openlocfilehash: 06a2bc48fa723f4d4513376cace96a195cef9fa3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316013"
---
# <a name="testing-following-and-stop-following-persons"></a>Testar o recurso de seguir e deixar de seguir pessoas

Este tópico descreve cenários para testar a capacidade do provedor do Outlook Social Connector (OSC) de seguir um amigo e para parar de seguir um amigo na rede social.
  
## <a name="following-a-person"></a>Seguindo uma pessoa

Para seguir uma pessoa é adicionar uma pessoa como amigo na rede social, usando o endereço SMTP fornecido pelo item selecionado do Outlook. A seguinte pessoa em uma rede social geralmente envolve a solicitação de permissão dessa pessoa por um email para esse endereço SMTP. Para conceder permissão, essa pessoa deve ter esse endereço SMTP já incluído em sua conta de rede social ou estar disposto a adicionar esse SMTP a uma conta de rede social. Teste cada um dos cenários a seguir para verificar se o provedor do OSC se comporta corretamente.
  
|**Cenário**|**Comportamento esperado**|
|:-----|:-----|
|Tentar seguir uma pessoa na rede social que existe na rede social.  <br/> |Para uma rede social que não requer permissão da pessoa, a rede social adiciona imediatamente a pessoa como um amigo.  <br/> Para uma rede que requer permissão dessa pessoa, a rede social envia uma notificação. O painel de pessoas do Outlook exibe um ícone pendente para essa pessoa.  <br/> |
|Tentar seguir uma pessoa na rede social que não existe na rede social.  <br/> |O provedor OSC exibe o erro apropriado no [ISocialSession:: FollowPerson](isocialsession-followperson.md) ou [ISocialSession2:: FollowPersonEx](isocialsession2-followpersonex.md).  <br/> |
|Seguindo um amigo na rede social.  <br/> |Para o amigo selecionado no painel de pessoas, o emblema da rede social e a imagem de perfil do amigo para essa rede social são exibidos.  <br/> |
|Selecionar o link para a página de perfil de um amigo.  <br/> |A página do amigo na rede social é aberta no navegador padrão do usuário conectado.  <br/> |
   
## <a name="stop-following-a-person"></a>Parar de seguir uma pessoa

Para parar de seguir uma pessoa é remover essa pessoa como amigo da rede social. Teste o cenário a seguir para verificar se seu provedor OSC para de seguir uma pessoa apropriadamente.
  
|**Cenário**|**Comportamento esperado**|
|:-----|:-----|
|Tentar remover uma pessoa como amigo na rede social.  <br/> |A rede social não lista mais essa pessoa como um amigo na conta do usuário conectado.  <br/> |
   
## <a name="see-also"></a>Confira também

- [Preparar um provedor de OSC para lançamento](getting-ready-to-release-an-osc-provider.md)

