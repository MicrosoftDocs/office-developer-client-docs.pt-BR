---
title: GUID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.GUID
api_type:
- COM
ms.assetid: e3608c47-06be-4476-a6ef-060fac252387
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 12c50ab5936d7fffd364c276ba07ca69d3459ae7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32299514"
---
# <a name="guid"></a>GUID

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Descreve um identificador global exclusivo (GUID). 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapiguid. h  <br/> |
   
```cpp
typedef struct _GUID
{
  unsigned long Data1;
  unsigned short Data2;
  unsigned short Data3;
  unsigned char Data4[8];
} GUID;

```

## <a name="members"></a>Members

 **Data1**
  
> Um valor de dados inteiro longo não assinado.
    
 **Data2**
  
> Um valor de dados inteiro curto não assinado.
    
 **Data3**
  
> Um valor de dados inteiro curto não assinado.
    
 **Data4**
  
> Uma matriz de caracteres não assinados.
    
## <a name="remarks"></a>Comentários

 Estruturas **GUID** são usadas em MAPI da seguinte maneira: 
  
- Nas estruturas [MAPIUID](mapiuid.md) que identificam exclusivamente os provedores de serviços. 
    
- Para identificadores de interface.
    
- No conjunto de propriedades, os nomes das propriedades nomeadas. 
    
O repositório de mensagens e os provedores de catálogo de endereços geram uma estrutura **GUID** para usar em sua estrutura **MAPIUID** . Ao passar o **MAPIUID** resultante para [IMAPISupport:: SetProviderUID](imapisupport-setprovideruid.md), esses provedores de serviços informam o MAPI de seu identificador exclusivo.
  
Além disso, eles são usados na implementação da RPC (chamada de procedimento remoto) da Microsoft e da linguagem de descrição de objeto (ODL). Para obter mais informações sobre esses usos, confira o *guia e referência do programador RPC da Microsoft*, *referência do programador do OLE* e *dentro do OLE*, *segunda edição* . 
  
A estrutura **GUID** é definida na *referência do programador do Win32* . Valores específicos para estruturas **GUID** usadas no MAPI são definidos no arquivo de cabeçalho MAPI Mapiguid. h. 
  
## <a name="see-also"></a>Confira também



[MAPIUID](mapiuid.md)


[Estruturas MAPI](mapi-structures.md)

