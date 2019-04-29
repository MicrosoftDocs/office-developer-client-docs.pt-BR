---
title: Exibir ícones de formulário
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 197e72ab-f9d6-4889-a677-0ce4c27b1aad
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: c93912d19f0ad3c3231092c82f27cec9e3f15b3e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438628"
---
# <a name="displaying-form-icons"></a>Exibir ícones de formulário

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Ao exibir uma lista de mensagens em uma pasta, é útil para os seus usuários se você distinguir mensagens com classes de mensagens personalizadas da IPM padrão. Mensagens de observação. As classes de mensagem personalizadas correspondem a servidores de formulários e os servidores de formulário fornecem ícones para serem representados por conta própria. Você pode exibir esses ícones na lista de mensagens para alertar os usuários sobre a classe de mensagem de cada mensagem antes de o usuário abrir as mensagens. Normalmente, o ícone na propriedade **PR_MINI_ICON** ([PidTagMiniIcon](pidtagminiicon-canonical-property.md)) do formulário é aquele que deve ser exibido na lista de mensagens. Formulários também têm uma propriedade **PR_ICON** ([PidTagIcon](pidtagicon-canonical-property.md)) que pode ser exibida quando o formulário é minimizado em uma folha de propriedades.
  
 **Para obter um ícone para uma classe de mensagem sem ativar o servidor de formulário para essa classe de mensagem**
  
1. Chame o método [IMAPIFormMgr:: OpenFormContainer](imapiformmgr-openformcontainer.md) para obter um ponteiro para uma interface [IMAPIFormContainer: IUnknown](imapiformcontaineriunknown.md) . 
    
2. Chame o método [IMAPIFormContainer:: ResolveMessageClass](imapiformcontainer-resolvemessageclass.md) para obter um ponteiro para uma interface [IMAPIFormInfo: IMAPIProp](imapiforminfoimapiprop.md) . 
    
3. Chame o método [IMAPIFormInfo:: MakeIconFromBinary](imapiforminfo-makeiconfrombinary.md) para obter uma alça de ícone. 
    
O ícone pode ser exibido usando as APIs padrão do Win32.
  
> [!IMPORTANT]
> Quando tiver o ícone de uma classe de mensagem, faça todos os esforços para armazenar em cache o ícone. Os ícones de não cache afetam seriamente o desempenho dos aplicativos cliente. Ao armazenar em cache ícones, cuidado com as relações entre as classes de mensagens e suas subclasses. Por exemplo, se IPM. Observação. Meeting. Cancel a classe de mensagem ocorre para resolver de volta para IPM. Observe que, não presuma que todas as subclasses IPM. Observação deve usar o ícone de IPM. Observação. 
  

