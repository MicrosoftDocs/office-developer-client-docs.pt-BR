---
title: Implementar uma função de ponto de entrada do provedor de serviços
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 83ff54c4-86ce-4529-ae45-260dfb763b30
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 14dd11f873493e32b83dbd1960cac8ff8ef8e436
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332988"
---
# <a name="implementing-a-service-provider-entry-point-function"></a>Implementar uma função de ponto de entrada do provedor de serviços

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Cada DLL do provedor de serviços tem uma função de ponto de entrada que o MAPI chama para carregá-lo. Lembre-se de que essa função de ponto de entrada não é igual a [DllMain](https://msdn.microsoft.com/library/ms682583.aspx), a função de ponto de entrada da dll Win32.
  
Dependendo do tipo de seu provedor, sua função de ponto de entrada do provedor está de acordo com um protótipo diferente. MAPI define diferentes protótipos de função de ponto de entrada para provedores de serviço.
  
|**Provider**|**Protótipo de função de ponto de entrada**|
|:-----|:-----|
|Provedores de repositórios de mensagens  <br/> |[MSProviderInit](msproviderinit.md) <br/> |
|Provedores de transporte  <br/> |[XPProviderInit](xpproviderinit.md) <br/> |
|Provedores de catálogo de endereços  <br/> |[ABProviderInit](abproviderinit.md) <br/> |
   
Grande parte da funcionalidade nesses protótipos é o mesmo para todos os tipos de provedor de serviços. 
  
Catálogo de endereços, repositório de mensagens e provedores de transporte execute as duas tarefas principais em suas funções de ponto de entrada:
  
1. Verifique a versão da interface do provedor de serviços (SPI) para certificar-se de que o MAPI está usando uma versão compatível com a versão que seu provedor de serviços está usando. Use o parâmetro _lpulMAPIVer_ , que contém a versão da SPI MAPI, e o parâmetro _lpulProviderVer_ , que contém sua versão SPI, para executar a verificação. Esses parâmetros são inteiros não assinados de 32 bits compostos de três partes: 
    
  - Os bits de 24 a 31 representam a versão principal.
    
  - Os bits 16 a 23 representam a versão secundária.
    
  - Os bits 0 a 15 representam o identificador de atualização. Embora o número de versão principal raramente seja alterado, o número da versão secundária é alterado sempre que MAPI é liberado e o SPI foi alterado. O identificador de atualização é a versão de compilação interna da Microsoft; é usado para controlar as alterações durante o processo de desenvolvimento. MAPI define a constante CURRENT_SPI_VERSION, documentada no arquivo de cabeçalho Mapispi. h, para indicar a versão da SPI atual. Falha ao verificar com o erro MAPI_E_VERSION se você estiver usando uma versão do SPI mais recente do que a versão que o MAPI está usando.
    
2. Criar uma instância de um objeto Provider. Como o provedor pode ser iniciado e inicializado várias vezes, você deve criar uma nova instância sempre que isso ocorrer. Os provedores são iniciados várias vezes quando aparecem em vários perfis que estão sendo usados simultaneamente por um ou mais clientes ou quando aparecem várias vezes em um único perfil. Assim como o protótipo de função de ponto de entrada difere dependendo do tipo de seu provedor, o tipo de objeto Provider. 
    
    Se você estiver escrevendo um provedor de catálogo de endereços, implemente [IABProvider: IUnknown](iabprovideriunknown.md). Se você estiver criando um provedor de armazenamento de mensagens, implemente [IMSProvider: IUnknown](imsprovideriunknown.md). Para obter mais informações, consulte [carregando provedores de repositório de mensagens](loading-message-store-providers.md).
    
    Se você estiver escrevendo um provedor de transporte, implemente [IXPProvider: IUnknown](ixpprovideriunknown.md). Para obter mais informações, consulte [inicializar o provedor de transporte](initializing-the-transport-provider.md).
    
## <a name="see-also"></a>Confira também



[Iniciar um provedor de serviços](starting-a-service-provider.md)

