---
title: Redigir uma nova mensagem usando um formulário
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c92181c4-79ca-4310-8bf1-2bc335c8e0cd
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 667d7afe1772786507ffc8eb75f901439ada61d3
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22587863"
---
# <a name="composing-a-new-message-by-using-a-form"></a>Redigir uma nova mensagem usando um formulário

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Para usar um formulário para redigir uma nova mensagem, primeiro crie um novo objeto de mensagem personalizada.
  
 **Para redigir uma nova mensagem usando um formulário**
  
1. Chamar o método de [IMAPIFormMgr::ResolveMessageClass](imapiformmgr-resolvemessageclass.md) do gerente de formulário para recuperar um ponteiro para um objeto de informações de formulário — um objeto que implementa o [IMAPIFormInfo: IMAPIProp](imapiforminfoimapiprop.md) interface. 
    
2. Passe o ponteiro para o objeto de informações de formulário em uma chamada para [IMAPIFormMgr::CreateForm](imapiformmgr-createform.md). **CreateForm** carrega o servidor de formulário apropriada. Além disso, passe um identificador de interface para **CreateForm** para especificar a interface para ser usado para acessar a nova mensagem. Normalmente, você solicitar [IPersistMessage: IUnknown](ipersistmessageiunknown.md) , passando IID_IPersistMessage para **CreateForm**.
    
3. Salve a nova mensagem chamando o método [IPersistMessage::Save](ipersistmessage-save.md) . O servidor do formulário deve definir valores para as propriedades da mensagem necessários quando ele cria a mensagem. 
    
4. Carregar a mensagem usando uma das duas estratégias: [IMAPIFormMgr::LoadForm](imapiformmgr-loadform.md) ou [PrepareForm](imapisession-prepareform.md) seguido [IMAPISession:: ShowForm](imapisession-showform.md). Para obter mais informações sobre essas estratégias, consulte [carregando uma mensagem em um formulário](loading-a-message-into-a-form.md).
    
> [!NOTE]
> Existem oportunidades para ganhos de desempenho ao carregar uma nova mensagem personalizada em um servidor de formulário, porque você já terá sido uma oportunidade de fazer algumas informações sobre a mensagem — como sua classe de mensagem — durante o processamento necessário para o ** ResolveMessageClass** e **CreateForm** chamadas. Dessa forma, você poderá simplificar o processamento necessário antes de chamar **LoadForm** sobre o que é descrito no tópico [carregando uma mensagem em um formulário](loading-a-message-into-a-form.md). 
  

