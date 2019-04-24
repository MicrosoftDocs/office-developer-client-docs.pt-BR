---
title: Inicializando o provedor de transporte
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 977c18ce-ece5-4ad1-ac97-5a680846ab83
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 474a8085ca8b82d11efd68c9fd4d8719fe239207
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309678"
---
# <a name="initializing-the-transport-provider"></a>Inicializando o provedor de transporte

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
A interface Transport-spooler define as chamadas feitas pelo spooler MAPI para um provedor de transporte. Os provedores de transporte implementam essas rotinas em uma biblioteca de vínculo dinâmico (DLL). O primeiro ponto de entrada direto na DLL usada pelo spooler MAPI deve ser a função de inicialização [XPProviderInit](xpproviderinit.md)do provedor de transporte.
  
MAPI usa a rotina de **GetProcAddress** para obter o endereço da rotina de inicialização do provedor de serviços e, em seguida, chama essa rotina. O nome da rotina de inicialização é **XPProviderInit** para provedores de transporte. É diferente para outros tipos de provedores de serviço MAPI, de forma que uma DLL possa conter qualquer combinação de tipos de provedor de serviços, mas apenas um provedor de serviços de um tipo específico. No enTanto, um provedor de serviços de um determinado tipo pode implementar vários serviços do seu tipo. Por exemplo, um provedor de transporte pode implementar a funcionalidade de transporte de mensagem para vários serviços de mensagens. 
  
O arquivo de cabeçalho mapispi. h tem uma definição de tipo para o protótipo de função da função de inicialização do provedor de transporte e um nome de procedimento predefinido para ele. Nomeando as rotinas de inicialização em seus arquivos C e C++ com os mesmos nomes usados por **GetProcAddress** e usando uma declaração de exportação direta em sua dll. DEF, você obtém automaticamente a verificação de tipo dos parâmetros na rotina de inicialização. Consulte o exemplo de código-fonte do provedor de transporte para obter exemplos. Para obter mais informações, consulte [Transport Provider Sample](transport-provider-sample.md).
  
Se uma chamada de inicialização do provedor de serviços for bem-sucedida, mas retornar um número de versão de interface do provedor de serviços muito pequeno para que o MAPI manipule, o MAPI chama imediatamente o método **Release** do objeto Service Provider e prossegue como se a chamada de inicialização falhou com MAPI_E_VERSION. Dessa forma, o MAPI e o provedor de serviços definem em conjunto o intervalo de números de versão da interface do provedor de serviços que eles podem manipular e, se não houver nenhuma correspondência, o carregamento do provedor de serviços falhará com um valor de retorno MAPI_E_VERSION. 
  
A última etapa do spooler MAPI em obter acesso aos recursos do provedor de serviços é fazer logon no provedor de transporte. O spooler MAPI chama o método [IXPProvider:: TransportLogon](ixpprovider-transportlogon.md) do objeto [IXPProvider: IUnknown](ixpprovideriunknown.md) retornado de **XPProviderInit**. Esta é a chamada na qual as credenciais, se usadas, são verificadas e as caixas de diálogo podem ser permitidas.
  
Se um processo abre uma segunda sessão de transporte no mesmo provedor de transporte e sessão MAPI, a DLL do provedor de transporte não deve criar um segundo objeto Provider. O primeiro objeto Provider deve ser usado para fazer logon na segunda sessão de transporte. Um provedor de transporte deve ser programado para dar suporte a várias sessões de transporte em um único objeto provedor. Um segundo objeto de provedor só deve ser criado se diferentes sessões MAPI forem usadas no mesmo processo.
  

