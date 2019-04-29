---
title: Iniciar um formulário para ler uma mensagem
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
# <a name="launching-a-form-to-read-a-message"></a>Iniciar um formulário para ler uma mensagem

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Os implementadores do servidor de formulários devem esperar a seguinte sequência de chamadas de método para o servidor de formulários e os objetos de formulário quando um aplicativo cliente carrega uma mensagem:
  
1. O aplicativo cliente abre o Gerenciador de formulários com uma chamada para a função [MAPIOpenFormMgr](mapiopenformmgr.md) . 
    
2. O aplicativo cliente chama o método [IMAPIFormMgr:: loadform](imapiformmgr-loadform.md) , que retorna um objeto com [IMAPIForm](imapiformiunknown.md). O Gerenciador de formulários pode ser liberado agora se não for usado para ativações de formulários adicionais. Observe que uma chamada para **loadform** pode levar algum tempo porque o Gerenciador de formulários pode ter que instalar os arquivos executáveis do servidor de formulário antes de prosseguir. 
    
3. Opcionalmente, o aplicativo cliente pode preparar o [IMAPIViewContext](imapiviewcontextiunknown.md) para controlar as operações que podem fazer com que o objeto Form carregue a mensagem anterior ou seguinte na pasta. O aplicativo cliente pode usar o método [IMAPIForm:: SetViewContext](imapiform-setviewcontext.md) para alterar o contexto de exibição padrão definido na chamada loadform. **** 
    
4. O aplicativo cliente chama o método [IPersistMessage:: Load](ipersistmessage-load.md) para carregar dados de mensagem no objeto Form. 
    
5. O aplicativo cliente chama [IMAPIForm::D overb](imapiform-doverb.md) para invocar o verbo Open, passando o ponteiro de interface opcional do [IMAPIViewContext](imapiviewcontextiunknown.md) . 
    
## <a name="see-also"></a>Confira também



[InterAções do servidor de formulário](form-server-interactions.md)

