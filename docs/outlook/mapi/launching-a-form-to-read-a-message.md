---
title: Iniciando um formulário para ler uma mensagem
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 54a4b805-2ab7-4fb7-b0ea-4a33ead27451
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 439927dc78941f086c025d77c76236497d3f4a15
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425929"
---
# <a name="launching-a-form-to-read-a-message"></a>Iniciando um formulário para ler uma mensagem

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Os implementadores de servidor de formulário devem esperar a seguinte sequência de chamadas de método para seus objetos de formulário e servidor de formulário quando um aplicativo cliente carregar uma mensagem:
  
1. O aplicativo cliente abre o gerenciador de formulário com uma chamada para a [função MAPIOpenFormMgr.](mapiopenformmgr.md) 
    
2. O aplicativo cliente chama o [método IMAPIFormMgr::LoadForm,](imapiformmgr-loadform.md) que retorna um objeto com [IMAPIForm](imapiformiunknown.md). O gerenciador de formulário pode ser liberado agora se não for usado para ativações de formulário posteriores. Observe que uma chamada para **LoadForm** pode levar algum tempo porque o gerenciador de formulário pode ter que instalar os arquivos executáveis do servidor de formulário antes de prosseguir. 
    
3. Opcionalmente, o aplicativo cliente pode preparar [IMAPIViewContext](imapiviewcontextiunknown.md) para controlar operações que podem fazer com que o objeto de formulário carregue a mensagem anterior ou a próxima na pasta. O aplicativo cliente pode usar o método [IMAPIForm::SetViewContext](imapiform-setviewcontext.md) para alterar o contexto de exibição padrão definido na **chamada LoadForm.** 
    
4. O aplicativo cliente chama o [método IPersistMessage::Load](ipersistmessage-load.md) para carregar dados de mensagem no objeto de formulário. 
    
5. O aplicativo cliente chama [IMAPIForm::D oVerb](imapiform-doverb.md) para invocar o verbo abrir, passando o ponteiro da interface [IMAPIViewContext](imapiviewcontextiunknown.md) opcional. 
    
## <a name="see-also"></a>Confira também



[Interações do Servidor de Formulário](form-server-interactions.md)

