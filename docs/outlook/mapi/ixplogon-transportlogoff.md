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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32351580"
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
  
> no Serve deve ser zero.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A chamada teve êxito e retornou o valor ou valores esperados. Se algo diferente de S_OK for retornado, o provedor será desconectado.
    
## <a name="remarks"></a>Comentários

O spooler MAPI chama o método **IXPLogon:: TransportLogoff** para encerrar uma sessão de provedor de transporte para um usuário específico. Antes de chamar **TransportLogoff**, o spooler MAPI descarta quaisquer dados sobre os tipos de endereço de mensagens suportados para esta sessão passadas pelo método [IXPLogon:: AddressTypes](ixplogon-addresstypes.md) . 
  
## <a name="notes-to-implementers"></a>Observações para implementadores

O provedor de transporte deve estar preparado para aceitar uma chamada para **TransportLogoff** a qualquer momento. Se uma mensagem estiver em processo, o provedor deverá interromper o processo de envio. 
  
O provedor de transporte deve liberar todos os recursos alocados para sua sessão atual. Se tiver alocado qualquer memória para esta sessão com a função [MAPIAllocateBuffer](mapiallocatebuffer.md) , deverá liberar a memória usando a função [MAPIFreeBuffer](mapifreebuffer.md) . Qualquer memória alocada pelo provedor de transporte para atender às chamadas para o método [IXPLogon:: AddressTypes](ixplogon-addresstypes.md) pode ser liberada com segurança no momento. 
  
Normalmente, ao concluir uma chamada **TransportLogoff** , um provedor deve primeiro invalidar seu objeto de logon chamando o método [IMAPISupport:: MakeInvalid](imapisupport-makeinvalid.md) e, em seguida, liberando o objeto de suporte. A implementação do provedor de **TransportLogoff** deve liberar o objeto support por último, porque quando o objeto support é liberado, o spooler MAPI também pode liberar o próprio objeto Provider. 
  
## <a name="see-also"></a>Confira também



[IMAPISupport::MakeInvalid](imapisupport-makeinvalid.md)
  
[IMAPISupport::SpoolerYield](imapisupport-spooleryield.md)
  
[IXPLogon::AddressTypes](ixplogon-addresstypes.md)
  
[MAPIAllocateBuffer](mapiallocatebuffer.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[IXPLogon : IUnknown](ixplogoniunknown.md)

