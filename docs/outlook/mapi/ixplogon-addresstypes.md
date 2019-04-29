---
title: IXPLogonAddressTypes
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IXPLogon.AddressTypes
api_type:
- COM
ms.assetid: 5add1f2b-d9e6-4d78-8739-c3848f6e32a3
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: ca68c604152a7a28fb6a5357aa9c012ec7466b5a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435373"
---
# <a name="ixplogonaddresstypes"></a>IXPLogon::AddressTypes

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Retorna os tipos de destinatários que o provedor de transporte manipula.
  
```cpp
HRESULT AddressTypes(
  ULONG FAR * lpulFlags,
  ULONG FAR * lpcAdrType,
  LPSTR FAR * FAR * lpppszAdrTypeArray,
  ULONG FAR * lpcMAPIUID,
  LPUID FAR * FAR * lpppUIDArray
);
```

## <a name="parameters"></a>Parâmetros

 _lpulFlags_
  
> bota Uma bitmask de sinalizadores que controla o tipo de cadeia de caracteres retornada. O seguinte sinalizador pode ser definido:
    
MAPI_UNICODE 
  
> As cadeias de caracteres retornadas estão no formato Unicode. Se o sinalizador MAPI_UNICODE não estiver definido, as cadeias de caracteres estarão no formato ANSI.
    
 _lpcAdrType_
  
> bota Um ponteiro para a contagem de entradas na matriz apontada pelo parâmetro _lpppszAdrTypeArray_ . 
    
 _lpppszAdrTypeArray_
  
> bota Um ponteiro para um ponteiro para uma matriz de cadeias de caracteres que identificam tipos de destinatários.
    
 _lpcMAPIUID_
  
> bota Um ponteiro para a contagem de entradas na matriz apontada pelo parâmetro _lpppUIDArray_ . 
    
 _lpppUIDArray_
  
> bota Um ponteiro para um ponteiro para uma matriz de ponteiros para estruturas [MAPIUID](mapiuid.md) que identificam os tipos de destinatários. 
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> O provedor de transporte indicou com êxito os tipos de destinatários que ele pode manipular.
    
## <a name="notes-to-implementers"></a>Observações para implementadores

O spooler MAPI chama o método **IXPLogon:: AddressTypes** imediatamente após um provedor de transporte retornar de uma chamada para o método [IXPProvider:: TransportLogon](ixpprovider-transportlogon.md) para que o provedor de transporte possa indicar quais tipos de destinatários ele manipula. Para indicar isso, o provedor de transporte deve passar de volta no parâmetro _lpppszAdrTypeArray_ um ponteiro para uma matriz de ponteiros para cadeias de caracteres ou passar de volta no parâmetro _lpppUIDArray_ um ponteiro para uma matriz de ponteiros para **MAPIUID** estruturas ou valores de passagem em ambos os parâmetros. 
  
Essas duas matrizes são usadas para diferentes processos de identificação. O MAPI e o spooler MAPI usam as estruturas [MAPIUID](mapiuid.md) na matriz _lpppUIDArray_ para identificar os identificadores de entrada de destinatários diretamente tratados pelo provedor de transporte ou pelo sistema de mensagens ao qual o provedor de transporte se conecta . Nem o MAPI nem o spooler MAPI expandem endereços usando identificadores de entrada contidos em qualquer uma dessas estruturas **MAPIUID** ; essas estruturas são usadas apenas para identificação de tipo de destinatário. 
  
O spooler MAPI usa cada cadeia de caracteres no parâmetro _lpppszAdrTypeArray_ para um teste de comparação quando decide qual provedor de transporte deve lidar com os destinatários de uma mensagem de saída. Se a propriedade **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)) de um destinatário de mensagem corresponder exatamente a uma cadeia de caracteres que identifica um dos tipos de endereço de mensagens que o provedor de transporte fornece, o provedor poderá entregar a mensagem para esse destinatário.
  
Se vários provedores de transporte puderem lidar com o mesmo tipo de destinatário, MAPI selecionará um provedor de transporte com base na ordem de prioridade de transporte indicada no perfil do aplicativo cliente. Para determinar qual provedor de transporte usar, o spooler MAPI examina todas as estruturas **MAPIUID** especificadas pelo provedor em ordem de prioridade e, em seguida, todos os valores de tipo de endereço especificados por provedor em ordem de prioridade. O primeiro provedor de transporte a corresponder a um determinado destinatário nesta verificação Obtém a primeira oportunidade para lidar com esse destinatário. Se esse provedor não manipular o destinatário, o spooler MAPI continuará a examinar para localizar um provedor de transporte para qualquer destinatário ainda não tratado. A verificação continua até que nenhuma outra correspondência seja encontrada, no ponto em que um relatório de não entrega é gerado para qualquer destinatário que não tenha sido manipulado. 
  
Se o provedor oferecer suporte a um determinado conjunto de tipos de destinatários, o tipo de endereço e as matrizes do **MAPIUID** que o provedor de transporte transmitir poderão ser estáticas. Se o provedor de transporte cria dinamicamente essas matrizes, ele pode alocar memória usando o objeto support que foi passado anteriormente na chamada para **TransportLogon**, embora isso não seja necessário.
  
A memória usada para o tipo de endereço e matrizes **MAPIUID** deve permanecer alocada até a chamada final para o método [IXPLogon:: TransportLogoff](ixplogon-transportlogoff.md) , no momento em que o provedor de transporte pode liberar a memória, se necessário. O provedor de transporte não deve alterar o conteúdo dessas matrizes depois de retornar da chamada **TransportLogoff** . 
  
Um provedor de transporte que pode manipular qualquer tipo de destinatário pode retornar NULL no parâmetro _lpppszAdrTypeArray_ . Provedores de transporte para sistemas de mensagens baseados em LAN que usam um servidor central para entregar mensagens de saída a vários sistemas de mensagens externos normalmente fazem isso. Esse tipo de provedor de transporte deve ser instalado por último na ordem de prioridade de MAPI e spooler MAPI dos provedores de transporte no perfil. 
  
Um provedor de transporte que não oferece suporte a mensagens de saída que foram despachadas com base no tipo de endereço deve retornar uma única sequência de comprimento zero no _lpppszAdrTypeArray_. Se um provedor de transporte não oferecer suporte a tipos de destinatários, ele deverá passar NULL para a estrutura **MAPIUID** e uma cadeia de caracteres vazia para o tipo de endereço. Provedores de transporte desse tipo são usados com mais frequência para instalar um pré-processador de mensagem. 
  
## <a name="see-also"></a>Confira também



[IXPLogon::TransportLogoff](ixplogon-transportlogoff.md)
  
[IXPProvider::TransportLogon](ixpprovider-transportlogon.md)
  
[MAPIUID](mapiuid.md)
  
[IXPLogon : IUnknown](ixplogoniunknown.md)

