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
ms.openlocfilehash: 08ecb718572944db07c2888e0aae1464bd5c0f98
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766670"
---
# <a name="guid"></a>GUID

  
  
**Aplica-se a**: Outlook 
  
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
  
> Um valor de dados de inteiro longo não assinado.
    
 **Data2**
  
> Um valor de dados de inteiro não assinado de curta.
    
 **Data3**
  
> Um valor de dados de inteiro não assinado de curta.
    
 **Data4**
  
> Uma matriz de caracteres não assinados.
    
## <a name="remarks"></a>Comentários

 Estruturas **GUID** são usadas na MAPI, da seguinte maneira: 
  
- Nas estruturas [MAPIUID](mapiuid.md) que identificam exclusivamente os provedores de serviços. 
    
- Para os identificadores de interface.
    
- Na propriedade define nomes de propriedades nomeadas. 
    
Armazenamento de mensagens e o endereço de provedores de catálogo geram uma estrutura **GUID** para usar em sua estrutura **MAPIUID** . Passando o resultante **MAPIUID** para [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md), esses provedores de serviço informam MAPI do seu identificador exclusivo.
  
Além disso, eles são usados na implementação do Microsoft Remote Procedure Call (RPC) e o idioma de descrição de objeto (ODL). Para obter mais informações sobre esses usos, consulte o *Guia do programador do Microsoft RPC e referência*, *referência do programador do OLE* e *Dentro OLE*, *Second Edition* . 
  
A estrutura **GUID** é definida na *referência do programador do Win32* . Valores específicos para estruturas **GUID** que são usados em MAPI são definidos no arquivo de cabeçalho MAPI Mapiguid.h. 
  
## <a name="see-also"></a>Confira também



[MAPIUID](mapiuid.md)


[Estruturas MAPI](mapi-structures.md)

