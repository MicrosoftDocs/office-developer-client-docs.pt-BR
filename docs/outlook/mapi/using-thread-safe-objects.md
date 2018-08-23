---
title: Usar objetos livres de threads
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: e688db5e-d1a1-4afc-998f-b3d31eb6239b
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 49a94b785a51b4b0c3082832145250eec0745a19
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22580975"
---
# <a name="using-thread-safe-objects"></a>Usar objetos livres de threads

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Aplicativos cliente podem assumir que os objetos usados diretamente ou como retornos de chamada são sempre thread-safe, exceto nos seguintes casos:
  
- Objeto de status de um provedor de transporte obtido por meio de uma chamada de cliente para [IMAPISession::OpenEntry](imapisession-openentry.md) com um identificador de entrada de linha de tabela de status do provedor. 
    
- Obtidos por meio de uma chamada de cliente para [MAPIOpenFormMgr](mapiopenformmgr.md)todos os objetos de formulário MAPI. Objetos de formulário cumprir regras de modelo apartment e os clientes devem usá-los e todos os objetos contidos por eles somente no segmento que foram criados.
    
Quando um cliente acessa a linha de um provedor de transporte na tabela de status que inclui o identificador de entrada do objeto status associado, o cliente pode chamar **OpenEntry** com esse identificador de entrada para abrir o objeto de status. Este objeto de status não é thread-safe porque os provedores de transporte executado no contexto do spooler MAPI e não mantêm um contexto separado para seu objeto de status. O objeto status obedeça a regras de modelo apartment e os clientes devem usar somente no segmento que criou a ele. 
  
Um cliente também deve chamar [MAPIInitialize](mapiinitialize.md) em cada segmento antes de usar quaisquer objetos MAPI e [MAPIUninitialize](mapiuninitialize.md) quando que usam for concluído. Essas chamadas devem ser feitas, mesmo se os objetos a serem usados são passados para o thread de uma fonte externa. **MAPIInitialize** e **MAPIUninitialize** podem ser chamado de qualquer lugar, exceto de dentro de uma função do Win32 **DllMain** , uma função que é invocada pelo sistema quando threads e processos são inicializados e encerradas, ou mediante chamadas para o ** LoadLibrary** e **FreeLibrary** funções. 
  
Usar indiretas objetos nunca devem ser considerados thread-safe. Usar indiretas objetos são retornados por métodos que requeiram ponteiros de interface de destino como parâmetros de entrada. Exemplos de tais métodos são **IMAPIProp::CopyTo** e **CopyProps**, **IMAPIFolder::CopyFolder** e **CopyMessage**e **IMsgServiceAdmin::CopyMsgService**. Se quiser que um provedor de serviços para um objeto desse tipo de chamada de um thread diferente em que ele foi passado, o provedor é responsável por marshaling explicitamente o objeto.
  

