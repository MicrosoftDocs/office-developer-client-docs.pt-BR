---
title: MapStorageSCode
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.MapStorageSCode
api_type:
- COM
ms.assetid: f686a2bc-aba5-4ea3-9963-76d0e96eab50
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: ab892513348541ec9de3c071a12268afa9337465
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19768039"
---
# <a name="mapstoragescode"></a>MapStorageSCode

  
  
**Aplica-se a**: Outlook 
  
Mapas de um SCODE retornam o valor de um objeto de armazenamento OLE para um tipo HRESULT. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |IMessage.h  <br/> |
|Implementada por:  <br/> |MAPI  <br/> |
|Chamado pelo:  <br/> |Provedores de serviços e aplicativos cliente  <br/> |
   
```cpp
SCODE MapStorageSCode(
  SCODE StgSCode
);
```

## <a name="parameters"></a>Parâmetros

 _StgSCode_
  
> [in] Valor de retorno de MAPI SCODE de um objeto de armazenamento OLE sejam mapeados para um valor HRESULT.
    
## <a name="return-value"></a>Valor retornado

S_OK 
  
> A chamada foi bem-sucedida e retornou o valor esperado.
    
MAPI_E_CALL_FAILED 
  
> A função não puder localizar um valor coincidente.
    
## <a name="remarks"></a>Comentários

MAPI fornece a função **MapStorageSCode** para uso interno de componentes MAPI que basear suas implementações de mensagem na mensagem de DLL. Porque esses componentes abrir o armazenamento OLE sozinhos, ele devem ser capaz de mapear os valores de erro retornados para problemas com o armazenamento OLE para um valor HRESULT. 
  
Para obter mais informações, consulte [Armazenamento estruturado](structured-storage-in-mapi.md). 
  

