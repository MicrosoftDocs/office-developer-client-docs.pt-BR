---
title: IXPLogonTransportLogoff
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IXPLogon.TransportLogoff
api_type:
- COM
ms.assetid: b2b368ce-4486-4f90-985f-59e50ca95229
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 761228a01e0dc778b962c62436e872ff20d72088
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22586309"
---
# <a name="ixplogontransportlogoff"></a>IXPLogon::TransportLogoff

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Inicia o processo de logoff. 
  
```cpp
HRESULT TransportLogoff(
  ULONG ulFlags
);
```

## <a name="parameters"></a>Parâmetros

 _ulFlags_
  
> [in] Reservado; deve ser zero.
    
## <a name="return-value"></a>Valor retornado

S_OK 
  
> A chamada foi bem-sucedida e retornou o valor esperado ou valores. Se qualquer coisa diferente de S_OK for retornada, o provedor será desconectado.
    
## <a name="remarks"></a>Comentários

O MAPI spooler chama o método **IXPLogon::TransportLogoff** para encerrar uma sessão do provedor de transporte para um usuário específico. Antes de chamar **TransportLogoff**, o MAPI spooler descarta quaisquer dados sobre tipos de endereço de mensagens com suporte para esta sessão passada no método [IXPLogon::AddressTypes](ixplogon-addresstypes.md) . 
  
## <a name="notes-to-implementers"></a>Notas para implementadores

O provedor de transporte deve estar preparado para aceitar uma chamada para **TransportLogoff** a qualquer momento. Se uma mensagem estiver em processo, o provedor deve parar o processo de envio. 
  
O provedor de transporte deve liberar todos os recursos alocados para a sua sessão atual. Se ele tiver qualquer memória alocada para esta sessão com a função [MAPIAllocateBuffer](mapiallocatebuffer.md) , ele deve liberar a memória usando a função [MAPIFreeBuffer](mapifreebuffer.md) . Toda a memória alocada pelo provedor de transporte para atender chamadas para o método [IXPLogon::AddressTypes](ixplogon-addresstypes.md) poderão ser liberada com segurança neste momento. 
  
Em geral, em Concluindo uma chamada **TransportLogoff** , um provedor deve primeiro invalidar seu objeto logon chamando o método [IMAPISupport::MakeInvalid](imapisupport-makeinvalid.md) e solte seu objeto de suporte. A implementação do provedor de **TransportLogoff** deve liberar o objeto de suporte ao último, porque quando o objeto de suporte é liberado, o MAPI spooler também pode liberar o próprio objeto de provedor. 
  
## <a name="see-also"></a>Confira também



[IMAPISupport::MakeInvalid](imapisupport-makeinvalid.md)
  
[IMAPISupport::SpoolerYield](imapisupport-spooleryield.md)
  
[IXPLogon::AddressTypes](ixplogon-addresstypes.md)
  
[MAPIAllocateBuffer](mapiallocatebuffer.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[IXPLogon : IUnknown](ixplogoniunknown.md)

