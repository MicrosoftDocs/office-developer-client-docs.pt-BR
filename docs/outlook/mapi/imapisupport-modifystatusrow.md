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
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 8c76e6059670e782ea6530ec8e94f77abfe5b9fe
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417158"
---
# <a name="imapisupportmodifystatusrow"></a>IMAPISupport::ModifyStatusRow

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Modifica a tabela de status adicionando uma nova linha ou modificando uma linha existente.
  
```cpp
HRESULT ModifyStatusRow(
ULONG cValues,
LPSPropValue lpColumnVals,
ULONG ulFlags
);
```

## <a name="parameters"></a>Parâmetros

 _cValues_
  
> [in] A contagem de propriedades a serem incluídas na linha da tabela de status nova ou modificada. 
    
 _lpColumnVals_
  
> [in] Um ponteiro para uma matriz de valores de propriedade que descrevem as propriedades a serem incluídas como colunas na linha de tabela de status nova ou modificada.
    
 _ulFlags_
  
> [in] Uma bitmask de sinalizadores que controla como as informações que definem a linha da tabela de status são processadas. O sinalizador a seguir pode ser definido:
    
STATUSROW_UPDATE 
  
> Direciona o MAPI para mesclar as propriedades incluídas na matriz apontada por  _lpColumnVals_ com uma linha de tabela de status existente, em vez de em uma nova linha. 
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A tabela de status foi atualizada com êxito.
    
## <a name="remarks"></a>Comentários

O **método IMAPISupport::ModifyStatusRow** é implementado para todos os objetos de suporte do provedor de serviços. Os provedores de serviços chamam **ModifyStatusRow** no momento do logon para adicionar uma linha à tabela de status e em outras ocasiões durante a sessão para atualizar a linha. **ModifyStatusRow** fornece MAPI com as informações necessárias para criar a tabela de status. 
  
## <a name="notes-to-callers"></a>Notas para chamadores

De definida STATUSROW_UPDATE sinalizador de status quando você chamar **ModifyStatusRow** para fazer alterações nas propriedades na linha da tabela de status existente. Isso informa AO MAPI que somente as colunas que estão sendo alteradas são passadas no parâmetro _lpColumnVals._ 
  
Os clientes podem usar as informações na tabela de status para acessar seu objeto de status. 
  
Para uma lista completa de colunas que você deve incluir na linha da tabela de status, consulte [Tabelas de Status.](status-tables.md)
  
## <a name="see-also"></a>Confira também



[IMAPISupport: IUnknown](imapisupportiunknown.md)

