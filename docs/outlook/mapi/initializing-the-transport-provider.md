---
title: Inicializando o Provedor de Transporte
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 977c18ce-ece5-4ad1-ac97-5a680846ab83
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 474a8085ca8b82d11efd68c9fd4d8719fe239207
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416598"
---
# <a name="initializing-the-transport-provider"></a>Inicializando o Provedor de Transporte

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
A interface transport-spooler define chamadas que o spooler MAPI faz a um provedor de transporte. Os provedores de transporte implementam essas rotinas em uma biblioteca de vínculo dinâmico (DLL). O primeiro ponto de entrada direta na DLL usada pelo spooler MAPI deve ser a função de inicialização do provedor de transporte [XPProviderInit](xpproviderinit.md).
  
MAPI uses the routine **GetProcAddress** to get the address of the service provider's initialization routine and then calls that routine. O nome da rotina de inicialização é **XPProviderInit** para provedores de transporte. É diferente para outros tipos de provedores de serviços MAPI para que uma DLL possa conter qualquer combinação de tipos de provedores de serviços, mas apenas um provedor de serviços de um tipo específico. No entanto, um provedor de serviços de um determinado tipo pode implementar vários serviços de seu tipo. Por exemplo, um provedor de transporte pode implementar a funcionalidade de transporte de mensagens em vários serviços de mensagens. 
  
O arquivo de header mapispi.h tem uma definição de tipo para o protótipo de função da função de inicialização do provedor de transporte e um nome de procedimento predefinido para ele. Ao nomear as rotinas de inicialização em seus arquivos C e C++ com os mesmos nomes usados por **GetProcAddress** e usando uma declaração de exportação simples em seu arquivo DLL.DEF, você recebe automaticamente a verificação de tipo dos parâmetros em sua rotina de inicialização. Consulte o código-fonte do provedor de transporte de exemplo para ver exemplos. Para obter mais informações, consulte [Exemplo de provedor de transporte.](transport-provider-sample.md)
  
Se a chamada de inicialização de um provedor de serviços for bem-sucedida, mas retornar um número de versão da interface do provedor de serviços muito pequeno para o MAPI manipular, o MAPI chamará imediatamente o método **Release** do objeto do provedor de serviços e prosseguirá como se a chamada de inicialização tivesse falhado com MAPI_E_VERSION. Dessa forma, o MAPI e o provedor de serviços definem em conjunto o intervalo de números de versão da interface do provedor de serviços que podem lidar e, se nada corresponde, o carregamento do provedor de serviços falha com um MAPI_E_VERSION de retorno. 
  
A última etapa para o spooler MAPI obter acesso aos recursos do provedor de serviços é fazer logoff no provedor de transporte. O spooler MAPI chama o método [IXPProvider::TransportLogon](ixpprovider-transportlogon.md) do [IXPProvider : objeto IUnknown](ixpprovideriunknown.md) retornado de **XPProviderInit**. Essa é a chamada em que as credenciais, se usadas, são marcadas e as caixas de diálogo podem ser permitidas.
  
Se um processo abrir uma segunda sessão de transporte no mesmo provedor de transporte e sessão MAPI, a DLL do provedor de transporte não deverá criar um segundo objeto de provedor. O primeiro objeto do provedor deve ser usado para fazer logon na segunda sessão de transporte. Um provedor de transporte deve ser programado para suportar várias sessões de transporte em um único objeto de provedor. Um segundo objeto de provedor só deve ser criado se diferentes sessões MAPI são usadas no mesmo processo.
  

