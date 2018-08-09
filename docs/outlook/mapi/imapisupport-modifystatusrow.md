---
title: IMAPISupportModifyStatusRow
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.ModifyStatusRow
api_type:
- COM
ms.assetid: a304ca8f-e404-4535-be76-0b673f2061a0
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 24718c50d02da5d60a6594f56ea6100650fe9f1a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767240"
---
# <a name="imapisupportmodifystatusrow"></a>IMAPISupport::ModifyStatusRow

  
  
**Aplica-se a**: Outlook 
  
Modifica a tabela de status, adicionando uma nova linha ou modificando uma linha existente.
  
```cpp
HRESULT ModifyStatusRow(
ULONG cValues,
LPSPropValue lpColumnVals,
ULONG ulFlags
);
```

## <a name="parameters"></a>Parâmetros

 _cValues_
  
> [in] A contagem de propriedades a serem incluídas na linha da tabela de status de novo ou modificado. 
    
 _lpColumnVals_
  
> [in] Um ponteiro para uma matriz de valores de propriedade que descrevem as propriedades a serem incluídos como colunas na linha da tabela de status de novo ou modificado.
    
 _ulFlags_
  
> [in] Uma bitmask dos sinalizadores que controla como as informações que definem a linha da tabela de status são processadas. O seguinte sinalizador pode ser definido:
    
STATUSROW_UPDATE 
  
> Direciona o MAPI para mesclar as propriedades incluídas na matriz apontado pela _lpColumnVals_ com uma linha de tabela de status existente, em vez de uma nova linha. 
    
## <a name="return-value"></a>Valor retornado

S_OK 
  
> A tabela de status foi atualizada com êxito.
    
## <a name="remarks"></a>Comentários

O método **IMAPISupport::ModifyStatusRow** é implementado para todos os objetos de suporte de provedor de serviço. Provedores de serviços de chamada **ModifyStatusRow** em tempo de logon para adicionar uma linha à tabela de status e em outros momentos durante a sessão para atualizar a linha. **ModifyStatusRow** fornece MAPI com as informações necessárias para criar a tabela de status. 
  
## <a name="notes-to-callers"></a>Notas para chamadores

Defina o sinalizador STATUSROW_UPDATE quando você chama **ModifyStatusRow** para fazer alterações nas propriedades em sua linha existente de tabela de status. Isso informa MAPI que somente as colunas que está sendo alteradas são passadas no parâmetro _lpColumnVals_ . 
  
Clientes podem usar as informações na tabela de status para acessar o objeto de status. 
  
Para obter uma lista completa das colunas que você deve incluir na sua linha da tabela de status, consulte [Tabelas de Status](status-tables.md).
  
## <a name="see-also"></a>Confira também



[IMAPISupport: IUnknown](imapisupportiunknown.md)

