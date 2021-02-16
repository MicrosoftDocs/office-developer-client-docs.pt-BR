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
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 78b4feeca263035b9c90184f10edd294e6cd7b10
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417858"
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
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A chamada foi bem-sucedida e retornou o valor ou os valores esperados. Se algo diferente S_OK for retornado, o provedor será desconectado.
    
## <a name="remarks"></a>Comentários

O spooler MAPI chama o **método IXPLogon::TransportLogoff** para encerrar uma sessão de provedor de transporte para um usuário específico. Antes de **chamar TransportLogoff**, o spooler MAPI descarta todos os dados sobre tipos de endereços de mensagens suportados para esta sessão passada no método [IXPLogon::AddressTypes.](ixplogon-addresstypes.md) 
  
## <a name="notes-to-implementers"></a>Observações para implementadores

O provedor de transporte deve estar preparado para aceitar uma chamada para **TransportLogoff** a qualquer momento. Se uma mensagem estiver em processo, o provedor deve interromper o processo de envio. 
  
O provedor de transporte deve liberar todos os recursos alocados para sua sessão atual. Se tiver alocado memória para esta sessão com a função [MAPIAllocateBuffer,](mapiallocatebuffer.md) ela deverá liberar a memória usando a função [MAPIFreeBuffer.](mapifreebuffer.md) Qualquer memória alocada pelo provedor de transporte para atender chamadas ao método [IXPLogon::AddressTypes](ixplogon-addresstypes.md) pode ser liberada com segurança neste momento. 
  
Normalmente, ao concluir uma chamada **TransportLogoff,** um provedor deve primeiro invalidar seu objeto de logon chamando o método [IMAPISupport::MakeInvalid](imapisupport-makeinvalid.md) e, em seguida, liberar seu objeto de suporte. A implementação do provedor de **TransportLogoff** deve liberar o objeto de suporte por último, porque quando o objeto de suporte é liberado, o spooler MAPI também pode liberar o próprio objeto do provedor. 
  
## <a name="see-also"></a>Confira também



[IMAPISupport::MakeInvalid](imapisupport-makeinvalid.md)
  
[IMAPISupport::SpoolerYield](imapisupport-spooleryield.md)
  
[IXPLogon::AddressTypes](ixplogon-addresstypes.md)
  
[MAPIAllocateBuffer](mapiallocatebuffer.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[IXPLogon : IUnknown](ixplogoniunknown.md)

