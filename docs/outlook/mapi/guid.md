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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421582"
---
# <a name="guid"></a>GUID

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Descreve um identificador global exclusivo (GUID). 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapiguid.h  <br/> |
   
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
  
> Um valor de dados de inteiro curto não assinado.
    
 **Data3**
  
> Um valor de dados de inteiro curto não assinado.
    
 **Data4**
  
> Uma matriz de caracteres não assinados.
    
## <a name="remarks"></a>Comentários

 **Estruturas GUID** são usadas em MAPI da seguinte forma: 
  
- Nas [estruturas MAPIUID](mapiuid.md) que identificam exclusivamente provedores de serviços. 
    
- Para identificadores de interface.
    
- Nos nomes de conjunto de propriedades de propriedades nomeadas. 
    
Os provedores de armazenamento de mensagens e de agendas geram uma estrutura **GUID** a ser usada em **sua estrutura MAPIUID.** Ao passar o **MAPIUID** resultante para [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md), esses provedores de serviços informam AO MAPI sobre seu identificador exclusivo.
  
Além disso, eles são usados na implementação da Chamada de Procedimento Remoto da Microsoft (RPC) e da ODL (Object Description Language). Para obter mais informações sobre esses usos, consulte o Guia e referência do programador do  *Microsoft RPC*, Referência do programador *OLE*  e  *Inside OLE*, *Segunda Edição*  . 
  
A **estrutura GUID** é definida na Referência do *programador do Win32.* Valores específicos para **estruturas GUID** que são usadas em MAPI são definidos no arquivo de header MAPI Mapiguid.h. 
  
## <a name="see-also"></a>Confira também



[MAPIUID](mapiuid.md)


[Estruturas MAPI](mapi-structures.md)

