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
|Arquivo de cabeçalho:  <br/> |IMessage. h  <br/> |
|Implementado por:  <br/> |MAPI  <br/> |
|Chamado por:  <br/> |Aplicativos cliente e provedores de serviços  <br/> |
   
```cpp
SCODE MapStorageSCode(
  SCODE StgSCode
);
```

## <a name="parameters"></a>Parâmetros

 _StgSCode_
  
> no SCODE MAPI valor de retorno de um objeto de armazenamento OLE a ser mapeado para um valor HRESULT.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A chamada teve êxito e retornou o valor esperado.
    
MAPI_E_CALL_FAILED 
  
> A função não pode localizar um valor correspondente.
    
## <a name="remarks"></a>Comentários

MAPI fornece a função **MapStorageSCode** para o uso interno de componentes MAPI que baseiam suas implementações de mensagem na DLL de mensagens. Como esses componentes abrem o armazenamento OLE, eles devem ser capazes de mapear valores de erro retornados para problemas com o armazenamento OLE para um valor HRESULT. 
  
Para obter mais informações, consulte [Structured Storage](structured-storage-in-mapi.md). 
  

