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
ms.openlocfilehash: 5dce5de820c07e1fa7b25b87d87993a30961b3f2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416521"
---
# <a name="mapstoragescode"></a>MapStorageSCode

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Mapeia um valor de retorno SCODE de um objeto de armazenamento OLE para um tipo HRESULT. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Imessage.h  <br/> |
|Implementado por:  <br/> |MAPI  <br/> |
|Chamado por:  <br/> |Aplicativos cliente e provedores de serviços  <br/> |
   
```cpp
SCODE MapStorageSCode(
  SCODE StgSCode
);
```

## <a name="parameters"></a>Parâmetros

 _StgSCode_
  
> [in] Valor de retorno de SCODE MAPI de um objeto de armazenamento OLE a ser mapeado para um valor HRESULT.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A chamada foi bem-sucedida e retornou o valor esperado.
    
MAPI_E_CALL_FAILED 
  
> A função não pode encontrar um valor correspondente.
    
## <a name="remarks"></a>Comentários

MAPI provides the **MapStorageSCode** function for the internal use of MAPI components that base their message implementations on the message DLL. Como esses componentes abrem o armazenamento OLE por conta própria, eles devem ser capazes de mapear os valores de erro retornados para problemas com o armazenamento OLE para um valor HRESULT. 
  
Para obter mais informações, consulte [Armazenamento Estruturado.](structured-storage-in-mapi.md) 
  

