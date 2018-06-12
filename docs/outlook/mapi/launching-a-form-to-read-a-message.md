---
title: Iniciando uma forma para ler uma mensagem
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 54a4b805-2ab7-4fb7-b0ea-4a33ead27451
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 675de7eeda534d8761887cdcb6d5c94a209ca18b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767764"
---
# <a name="launching-a-form-to-read-a-message"></a>Iniciando uma forma para ler uma mensagem

  
  
**Aplica-se a**: Outlook 
  
Implementadores de servidor do formulário devem esperar que a seguinte sequência de chamadas de método para seus servidores do formulário e seus objetos de formulário quando um aplicativo cliente carrega uma mensagem:
  
1. O aplicativo cliente abre o Gerenciador de formulário com uma chamada para a função [MAPIOpenFormMgr](mapiopenformmgr.md) . 
    
2. O aplicativo cliente chama o método [IMAPIFormMgr::LoadForm](imapiformmgr-loadform.md) , que retorna um objeto com [IMAPIForm](imapiformiunknown.md). O gerente de formulário pode ser lançado agora se ela não será usada para outras ativações de formulário. Observe que uma chamada para **LoadForm** pode levar algum tempo porque o Gerenciador de formulário talvez seja necessário instalar os arquivos executáveis do servidor formulário antes de continuar. 
    
3. Opcionalmente, o aplicativo cliente pode preparar [IMAPIViewContext](imapiviewcontextiunknown.md) para controlar operações que podem causar o objeto de formulário carregar a mensagem anterior ou seguinte na pasta. O aplicativo cliente pode usar o método [IMAPIForm::SetViewContext](imapiform-setviewcontext.md) para alterar o contexto de modo de exibição padrão que foi definido na chamada **LoadForm** . 
    
4. O aplicativo cliente chama o método [IPersistMessage::Load](ipersistmessage-load.md) para carregar dados de mensagem no objeto form. 
    
5. O aplicativo cliente chama [IMAPIForm::DoVerb](imapiform-doverb.md) para invocar o verbo open, passando o ponteiro de interface [IMAPIViewContext](imapiviewcontextiunknown.md) opcional. 
    
## <a name="see-also"></a>Confira também



[Interações do servidor de formulário](form-server-interactions.md)

