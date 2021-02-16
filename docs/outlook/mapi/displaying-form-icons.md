---
title: Exibindo ícones de formulário
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
# <a name="displaying-form-icons"></a>Exibindo ícones de formulário

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Ao exibir uma lista de mensagens em uma pasta, será útil para os usuários distinguir mensagens com classes de mensagens personalizadas do IPM padrão. Anotações de mensagens. As classes de mensagens personalizadas correspondem a servidores de formulário, e os servidores de formulário fornecem ícones para representarem a si mesmos. Você pode exibir esses ícones na lista de mensagens para alertar os usuários sobre a classe de mensagens de cada mensagem antes que o usuário abra as mensagens. Normalmente, o ícone na propriedade **PR_MINI_ICON** ([PidTagMiniIcon](pidtagminiicon-canonical-property.md)) do formulário é aquele que deve ser exibido na lista de mensagens. Forms also have a **PR_ICON** ([PidTagIcon](pidtagicon-canonical-property.md)) property that can be displayed when the form is minimized in a property sheet.
  
 **Para obter um ícone para uma classe de mensagem sem ativar o servidor de formulário para essa classe de mensagem**
  
1. Chame o [método IMAPIFormMgr::OpenFormContainer](imapiformmgr-openformcontainer.md) para obter um ponteiro para [um IMAPIFormContainer : interface IUnknown.](imapiformcontaineriunknown.md) 
    
2. Chame o [método IMAPIFormContainer::ResolveMessageClass](imapiformcontainer-resolvemessageclass.md) para obter um ponteiro para [uma interface IMAPIFormInfo : IMAPIProp.](imapiforminfoimapiprop.md) 
    
3. Chame o [método IMAPIFormInfo::MakeIconFromBinary](imapiforminfo-makeiconfrombinary.md) para obter uma alça de ícone. 
    
Em seguida, o ícone pode ser exibido usando APIs win32 padrão.
  
> [!IMPORTANT]
> Depois de ter o ícone de uma classe de mensagem, faça todo o esforço para armazenar em cache esse ícone. Não o armazenamento em cache de ícones afeta gravemente o desempenho dos aplicativos cliente. Ao cache de ícones, tenha cuidado com as relações entre classes de mensagem e suas subclasses. Por exemplo, se o IPM. Note.Meeting.Cancel message class happens to resolve back to IPM. Observação, não suponha que todas as subclasses do IPM. A observação deve usar o ícone do IPM. Observação. 
  

