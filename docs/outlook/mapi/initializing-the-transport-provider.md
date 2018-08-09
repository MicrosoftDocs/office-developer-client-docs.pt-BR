---
title: Inicializar o provedor de transporte
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 977c18ce-ece5-4ad1-ac97-5a680846ab83
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 423b03d674028a2f81b4c042d6e65e9acfb57274
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767567"
---
# <a name="initializing-the-transport-provider"></a>Inicializar o provedor de transporte

  
  
**Aplica-se a**: Outlook 
  
A interface de transporte-spooler define o MAPI spooler torna a um provedor de transporte de chamadas. Provedores de transporte implementam essas rotinas em uma biblioteca de vínculo dinâmico (DLL). O primeiro ponto de entrada direta a DLL usado pelo spooler MAPI deve ser a função de inicialização do provedor de transporte [XPProviderInit](xpproviderinit.md).
  
Usa a rotina **GetProcAddress** para obter o endereço de rotina de inicialização do provedor de serviços e, em seguida, chama esse rotina MAPI. O nome da rotina de inicialização é **XPProviderInit** para provedores de transporte. É diferente de outros tipos de provedores de serviço MAPI para que uma DLL pode conter qualquer combinação de tipos de provedor de serviço, mas apenas um provedor de serviços de um determinado tipo. No entanto, um provedor de serviços de um determinado tipo pode implementar vários serviços de seu tipo. Por exemplo, um provedor de transporte pode implementar o recurso de transporte de mensagens para vários serviços de mensagem. 
  
O arquivo de cabeçalho mapispi.h tem uma definição de tipo para o protótipo de função da função de inicialização de provedor de transporte e um nome de procedimento predefinido para ele. Nomeando as rotinas de inicialização em seus arquivos C e C++ com nomes iguais aos usados pelo **GetProcAddress** e usando um simples exporte declaração na sua DLL. Arquivo DEF, você obterá automaticamente verificação dos parâmetros na sua rotina de inicialização do tipo. Consulte o código de origem do provedor de transporte amostra para obter exemplos. Para obter mais informações, consulte [Sample do provedor de transporte](transport-provider-sample.md).
  
Se chamada de inicialização de um provedor de serviços for bem-sucedido, mas retorna um provedor de serviços número da versão de interface muito pequeno para MAPI lidar com, MAPI imediatamente chama o método de **lançamento** do objeto de provedor de serviço e continua como se a inicialização de chamada tinha falhou com MAPI_E_VERSION. Dessa maneira, MAPI e o provedor de serviço em conjunto definem o intervalo de números de versão do serviço provedor interface podem lidar com e se nada faz a correspondência de carregamento do provedor de serviços falhar com um MAPI_E_VERSION valor de retorno. 
  
A última etapa para o MAPI spooler na obtenção de acesso aos recursos do provedor de serviço é para fazer logon no provedor de transporte. O MAPI spooler chama o método [IXPProvider::TransportLogon](ixpprovider-transportlogon.md) do [IXPProvider: IUnknown](ixpprovideriunknown.md) objeto retornado de **XPProviderInit**. Esta é a chamada onde credenciais, se for usado, serão verificadas e caixas de diálogo podem ser permitidas.
  
Se um processo abre uma segunda sessão de transporte, o mesmo provedor de transporte e sessão MAPI, o provedor de transporte DLL não deve criar um segundo objeto de provedor. O primeiro objeto do provedor deve ser usado para fazer logon para a segunda sessão de transporte. Um provedor de transporte deve ser programado para dar suporte a várias sessões de transporte em um objeto único provedor. Um segundo objeto de provedor deve apenas ser criado se diferentes sessões MAPI são usadas no mesmo processo.
  

