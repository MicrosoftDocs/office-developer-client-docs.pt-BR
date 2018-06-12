---
title: Implementando uma função de ponto de entrada de provedor de serviço
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 83ff54c4-86ce-4529-ae45-260dfb763b30
description: '�ltima altera��o: segunda-feira, 9 de mar�o de 2015'
ms.openlocfilehash: 632aff9c0f6fc60ee9730b5e43667b5b610ae8df
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767412"
---
# <a name="implementing-a-service-provider-entry-point-function"></a>Implementando uma função de ponto de entrada de provedor de serviço

  
  
**Aplica-se a**: Outlook 
  
Cada DLL do provedor de serviço tem uma entrada aponte a função que chamadas MAPI carregá-la. Lembre-se de que essa função de ponto de entrada não é igual ao [DllMain](http://msdn.microsoft.com/en-us/library/ms682583.aspx), a função do ponto de entrada DLL Win32.
  
Dependendo do tipo do seu provedor, sua função de ponto de entrada do provedor está em conformidade com um protótipo diferente. MAPI define protótipos de função de ponto de entrada diferentes para provedores de serviços.
  
|**Provider**|**Protótipo de função de ponto de entrada**|
|:-----|:-----|
|Provedores de armazenamento de mensagem  <br/> |[MSProviderInit](msproviderinit.md) <br/> |
|Provedores de transporte  <br/> |[XPProviderInit](xpproviderinit.md) <br/> |
|Provedores de catálogo de endereços  <br/> |[ABProviderInit](abproviderinit.md) <br/> |
   
Muitas das funcionalidades nesses protótipos é o mesmo para todos os tipos de provedor de serviço. 
  
Catálogo de endereços, armazenamento de mensagens e provedores de transporte executam duas tarefas principais a seguir em suas funções de ponto de entrada:
  
1. Verifica a versão da interface do provedor de serviço (SPI) para certificar-se de que o MAPI está usando uma versão compatível com a versão que está usando o seu provedor de serviços. Use o parâmetro _lpulMAPIVer_ , que contém a versão de MAPI SPI e o parâmetro _lpulProviderVer_ , que contém sua versão EDA, executar a verificação. Estes parâmetros são números inteiros não assinados de 32 bits compostos de três partes: 
    
  - Bits 24 a 31 representam a versão principal.
    
  - Bits 16 a 23 representam a versão secundária.
    
  - Bits 0 a 15 representam o identificador de atualização. Embora raramente altera o número da versão principal, a número da versão secundária alterações sempre que o MAPI é liberada e o SPI foi alterada. O identificador de atualização é a versão; de compilação do Microsoft interno ele é usado para rastrear alterações durante o processo de desenvolvimento. MAPI define a constante CURRENT_SPI_VERSION, documentados no arquivo de cabeçalho Mapispi.h, para indicar a versão de EDA presente. Falha de sua verificação com o erro MAPI_E_VERSION se você estiver usando uma versão da SPI mais recente que a versão que está usando o MAPI.
    
2. Crie uma instância de um objeto do provedor. Porque seu provedor pode ser iniciado e inicializado várias vezes, você deve criar uma nova instância sempre que isso ocorre. Provedores são iniciados várias vezes quando eles aparecem em vários perfis que estiverem em uso simultaneamente por um ou mais clientes ou quando eles aparecem várias vezes em um único perfil. Assim como o protótipo de função de ponto de entrada será diferente, dependendo do tipo de seu provedor, portanto não o tipo de objeto do provedor. 
    
    Se você estiver escrevendo um provedor de catálogo de endereços, implemente [IABProvider: IUnknown](iabprovideriunknown.md). Se você estiver escrevendo um provedor de armazenamento de mensagem, implemente [IMSProvider: IUnknown](imsprovideriunknown.md). Para obter mais informações, consulte [Carregando provedores de armazenamento de mensagem](loading-message-store-providers.md).
    
    Se você estiver escrevendo um provedor de transporte, implemente [IXPProvider: IUnknown](ixpprovideriunknown.md). Para obter mais informações, consulte [inicializar o provedor de transporte](initializing-the-transport-provider.md).
    
## <a name="see-also"></a>Confira também



[Iniciando um provedor de serviços](starting-a-service-provider.md)

