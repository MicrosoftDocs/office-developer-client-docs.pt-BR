---
title: Composição de uma nova mensagem usando um formulário
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c92181c4-79ca-4310-8bf1-2bc335c8e0cd
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 1c5ba8631ba39309b7131440f04564f80b5dbb57
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412797"
---
# <a name="composing-a-new-message-by-using-a-form"></a>Composição de uma nova mensagem usando um formulário

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Para usar um formulário para redigir uma nova mensagem, primeiro crie um novo objeto de mensagem personalizado.
  
 **Para redigir uma nova mensagem usando um formulário**
  
1. Chame o método [IMAPIFormMgr::ResolveMessageClass](imapiformmgr-resolvemessageclass.md) do gerenciador de formulário para recuperar um ponteiro para um objeto de informações de formulário — um objeto que implementa a interface [IMAPIFormInfo : IMAPIProp.](imapiforminfoimapiprop.md) 
    
2. Passe o ponteiro para o objeto de informações do formulário em uma chamada para [IMAPIFormMgr::CreateForm](imapiformmgr-createform.md). **CreateForm** carrega o servidor de formulário apropriado. Além disso, passe um identificador de interface para **CreateForm** para especificar a interface a ser usada para acessar a nova mensagem. Normalmente, você solicita [IPersistMessage : IUnknown](ipersistmessageiunknown.md) passando IID_IPersistMessage para **CreateForm**.
    
3. Salve a nova mensagem chamando seu [método IPersistMessage::Save.](ipersistmessage-save.md) O servidor de formulário deve definir valores para as propriedades necessárias da mensagem ao criar a mensagem. 
    
4. Carregue a mensagem usando uma de duas estratégias: [IMAPIFormMgr::LoadForm](imapiformmgr-loadform.md) ou [IMAPISession::P repareForm](imapisession-prepareform.md) seguido de [IMAPISession::ShowForm](imapisession-showform.md). Para obter mais informações sobre essas estratégias, consulte [Carregando uma mensagem em um formulário.](loading-a-message-into-a-form.md)
    
> [!NOTE]
> Há oportunidades de ganhos de desempenho ao carregar uma nova mensagem personalizada em um servidor de formulário porque você já terá a oportunidade de obter algumas informações sobre a mensagem — como sua classe de mensagem — durante o processamento necessário para as chamadas **ResolveMessageClass** e **CreateForm.** Por isso, você poderá simplificar o processamento necessário antes de chamar **LoadForm** sobre o que descrito no tópico [Loading a Message Into a Form](loading-a-message-into-a-form.md). 
  

