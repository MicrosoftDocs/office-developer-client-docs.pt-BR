---
title: Usando objetos isentos de threads
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: e688db5e-d1a1-4afc-998f-b3d31eb6239b
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 611e0a49f0fd8df8fe40205a33ed5501055c3d45
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425166"
---
# <a name="using-thread-safe-objects"></a>Usando objetos isentos de threads

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Os aplicativos cliente podem supor que os objetos usados diretamente ou como retornos de chamada sejam sempre thread-safe, exceto nos seguintes casos:
  
- Um objeto de status de um provedor de transporte obtido por meio de uma chamada de cliente para [IMAPISession:: OpenEntry](imapisession-openentry.md) com um identificador de entrada da linha da tabela de status do provedor. 
    
- Todos os objetos Form MAPI obtidos por meio de uma chamada de cliente para o [MAPIOpenFormMgr](mapiopenformmgr.md). Os objetos de formulário obedecem às regras de modelo de apartamento e os clientes devem usá-los e todos os objetos contidos neles somente no thread que os criou.
    
Quando um cliente acessa uma linha de um provedor de transporte na tabela de status que inclui o identificador de entrada do objeto de status associado, o cliente pode chamar **OpenEntry** com esse identificador de entrada para abrir o objeto status. Esse objeto status não é thread-safe porque os provedores de transporte são executados no contexto do spooler MAPI e não mantêm um contexto separado para o objeto status. O objeto status obedece às regras de modelo de apartamento e os clientes devem usá-la somente no thread que a criou. 
  
Um cliente também deve invocar O [MAPIInitialize](mapiinitialize.md) em todos os threads antes de usar qualquer objeto MAPI e [MAPIUninitialize](mapiuninitialize.md) quando o uso estiver concluído. Essas chamadas devem ser feitas mesmo se os objetos a serem usados são passados para o thread de uma fonte externa. **MAPIInitialize** e **MAPIUninitialize** podem ser chamados de qualquer lugar, exceto de dentro de uma função **DllMain** do Win32, uma função que é invocada pelo sistema quando processos e threads são inicializados e finalizados, ou quando chamadas para o ** Funções LoadLibrary** e **FreeLibrary** . 
  
Os objetos de uso inDireto nunca devem ser considerados isentos de threads. Os objetos de uso inDireto são retornados por métodos que exigem ponteiros de interface de destino como parâmetros de entrada. Exemplos desses métodos são **IMAPIProp:: CopyTo** e **CopyProps**, **IMAPIFolder:: CopyFolder** e **CopyMessage**, e **IMsgServiceAdmin:: CopyMsgService**. Se um provedor de serviços quiser chamar esse objeto de um thread diferente daquele no qual foi passado, o provedor será responsável por empacotar explicitamente o objeto.
  

