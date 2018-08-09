---
title: Exibir ícones de formulário
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 197e72ab-f9d6-4889-a677-0ce4c27b1aad
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: b2e79e5568de38bee9a97c9df2598b30f1ba1bdf
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766432"
---
# <a name="displaying-form-icons"></a>Exibir ícones de formulário

  
  
**Aplica-se a**: Outlook 
  
Ao exibir uma lista de mensagens em uma pasta, é útil para os usuários se você distinguir mensagens com classes de mensagem personalizada do standard IPM. Observe as mensagens. Classes de mensagem personalizada correspondem aos servidores de formulário, e os servidores de formulário fornecem ícones para representar a próprios. Você pode exibir esses ícones na lista de mensagens para alertar os usuários à classe de mensagem de cada mensagem antes do usuário abrir as mensagens. Normalmente, o ícone na propriedade de **PR_MINI_ICON** ([PidTagMiniIcon](pidtagminiicon-canonical-property.md)) do formulário é aquela que deve ser exibida na lista de mensagens. Formulários também têm uma propriedade de **PR_ICON** ([PidTagIcon](pidtagicon-canonical-property.md)) que pode ser exibida quando o formulário é minimizado em uma folha de propriedades.
  
 **Para obter um ícone para uma classe de mensagem sem ativar o servidor de formulário para essa classe de mensagem**
  
1. Chame o método [IMAPIFormMgr::OpenFormContainer](imapiformmgr-openformcontainer.md) para obter um ponteiro para uma [IMAPIFormContainer: IUnknown](imapiformcontaineriunknown.md) interface. 
    
2. Chame o método [IMAPIFormContainer::ResolveMessageClass](imapiformcontainer-resolvemessageclass.md) para obter um ponteiro para uma [IMAPIFormInfo: IMAPIProp](imapiforminfoimapiprop.md) interface. 
    
3. Chame o método [IMAPIFormInfo::MakeIconFromBinary](imapiforminfo-makeiconfrombinary.md) para obter um identificador de ícone. 
    
O ícone pode ser exibido usando APIs do Win32 padrão.
  
> [!IMPORTANT]
> Depois que você tiver o ícone de uma classe de mensagem, fazer todos os esforços para armazenar em cache nesse ícone. Não cache ícones está seriamente afeta o desempenho dos aplicativos cliente. Ao cache ícones, tenha cuidado das relações entre as classes de mensagens e suas subclasses. Por exemplo, se o formulário IPM. Classe de mensagem Note.Meeting.Cancel acontece resolver novamente IPM. Observação, não presuma que todas as subclasses da IPM. Observação deve usar o ícone para IPM. Nota. 
  

