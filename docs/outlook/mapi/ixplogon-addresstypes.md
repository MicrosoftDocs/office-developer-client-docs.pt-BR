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
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: a7bb1aca501e24843950114bb76b6a09b20f2467
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767742"
---
# <a name="ixplogonaddresstypes"></a>IXPLogon::AddressTypes

  
  
**Aplica-se a**: Outlook 
  
Retorna os tipos de destinatários que processa o provedor de transporte.
  
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
  
> [out] Uma bitmask dos sinalizadores que controla o tipo de cadeias de caracteres retornada. O seguinte sinalizador pode ser definido:
    
MAPI_UNICODE 
  
> As cadeias de caracteres retornadas estão no formato Unicode. Se o sinalizador MAPI_UNICODE não estiver definido, as cadeias de caracteres estão no formato ANSI.
    
 _lpcAdrType_
  
> [out] Um ponteiro para a contagem de entradas na matriz apontado pelo parâmetro _lpppszAdrTypeArray_ . 
    
 _lpppszAdrTypeArray_
  
> [out] Um ponteiro para um ponteiro para uma matriz de cadeias de caracteres que identificam os tipos de destinatário.
    
 _lpcMAPIUID_
  
> [out] Um ponteiro para a contagem de entradas na matriz apontado pelo parâmetro _lpppUIDArray_ . 
    
 _lpppUIDArray_
  
> [out] Um ponteiro para um ponteiro para uma matriz de ponteiros para estruturas [MAPIUID](mapiuid.md) que identificam os tipos de destinatário. 
    
## <a name="return-value"></a>Valor retornado

S_OK 
  
> O provedor de transporte com êxito indicado os tipos de destinatários que pode manipular.
    
## <a name="notes-to-implementers"></a>Notas para implementadores

O MAPI spooler chama o método de **IXPLogon::AddressTypes** imediatamente depois que um provedor de transporte retorna de uma chamada para o método [IXPProvider::TransportLogon](ixpprovider-transportlogon.md) para que o provedor de transporte pode indicar quais tipos de destinatários que ele manipula. Para indicar que isso, o provedor de transporte deve passar novamente no parâmetro _lpppszAdrTypeArray_ um ponteiro para uma matriz de ponteiros para as cadeias de caracteres ou passar novamente no parâmetro _lpppUIDArray_ um ponteiro para uma matriz de ponteiros para **MAPIUID** estruturas ou valores de passagem em ambos os parâmetros. 
  
Essas duas matrizes são usados para processos de identificação diferente. MAPI e o MAPI spooler usam as estruturas [MAPIUID](mapiuid.md) na matriz _lpppUIDArray_ para identificar os identificadores de entrada do destinatário diretamente são manipulados pelo provedor de transporte ou pelo sistema de mensagens ao qual se conecta o provedor de transporte . Nem MAPI nem o MAPI spooler expande endereços usando identificadores de entrada contidos em qualquer uma dessas estruturas **MAPIUID** ; Essas estruturas são usadas apenas para a identificação do tipo de destinatário. 
  
O MAPI spooler usa cada uma das cadeias de caracteres no parâmetro _lpppszAdrTypeArray_ para um teste de comparação quando ela decide qual provedor de transporte deve lidar com quais destinatários para uma mensagem de saída. Se a propriedade de **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)) de um destinatário de mensagem corresponde exatamente a uma cadeia de caracteres que identifica um dos tipos de endereço de mensagens que o provedor de transporte fornece, o provedor pode entregar a mensagem para que o destinatário.
  
Se vários provedores de transporte podem lidar com o mesmo tipo de destinatário, MAPI seleciona um provedor de transporte com base na ordem de prioridade de transporte indicada no perfil do aplicativo cliente. Para determinar qual provedor de transporte a ser usado, o MAPI spooler examina todas as estruturas **MAPIUID** provedor especificado em ordem de prioridade e, em seguida, todos os endereços especificados pelo provedor tipo valores em ordem de prioridade. O primeiro provedor de transporte para corresponder a um determinado destinatário neste exame obtém a primeira oportunidade para lidar com o destinatário. Se o provedor não manipular o destinatário, o MAPI spooler continua a varredura para localizar um provedor de transporte de qualquer destinatário ainda não foram tratado. O exame continua até que nenhuma correspondência adicional forem encontradas, nesse momento é gerado um relatório de não entrega para qualquer destinatário que não foi tratado. 
  
Se o provedor sempre oferece suporte a um determinado conjunto de tipos de destinatário, o tipo de endereço e matrizes **MAPIUID** que o provedor de transporte passado podem ser estáticos. Se o provedor de transporte dinamicamente constrói desses conjuntos, ele pode alocar memória usando o objeto de suporte anteriormente passado na chamada a **TransportLogon**, embora isso não é necessário.
  
A memória usada para o tipo de endereço e **MAPIUID** matrizes deve permanecer alocada até que a chamada final para o método [IXPLogon::TransportLogoff](ixplogon-transportlogoff.md) , no momento em que o provedor de transporte pode liberar a memória, se necessário. O provedor de transporte não deverá alterar o conteúdo desses conjuntos após ela retornar da chamada **TransportLogoff** . 
  
Um provedor de transporte que pode lidar com qualquer tipo de destinatário pode retornar NULL no parâmetro _lpppszAdrTypeArray_ . Provedores de transporte para sistemas de mensagens baseado em LAN que usa um servidor central para entregar mensagens enviadas para vários sistemas de mensagem estrangeira comumente fazer isso. Esse tipo de provedor de transporte deve ser instalado por último na MAPI e MAPI ordem de prioridade de spooler de provedores de transporte no perfil. 
  
Um provedor de transporte que não oferece suporte a mensagens de saída que são enviadas a ela com base no tipo de endereço deve retornar uma única cadeia de caracteres de comprimento zero em _lpppszAdrTypeArray_. Se um provedor de transporte não suporta nenhum tipo de destinatário, ele deve passar NULL para a estrutura **MAPIUID** e uma cadeia de caracteres vazia para o tipo de endereço. Provedores de transporte desse tipo são mais comumente usadas para instalar um pré-processador de mensagem. 
  
## <a name="see-also"></a>Confira também



[IXPLogon::TransportLogoff](ixplogon-transportlogoff.md)
  
[IXPProvider::TransportLogon](ixpprovider-transportlogon.md)
  
[MAPIUID](mapiuid.md)
  
[IXPLogon : IUnknown](ixplogoniunknown.md)

