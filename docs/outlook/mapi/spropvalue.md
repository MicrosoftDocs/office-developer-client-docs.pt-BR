---
title: SPropValue
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SPropValue
api_type:
- COM
ms.assetid: faf795a2-84db-432d-a05f-082f25a5cab5
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: c7f4e8835831af6277cef134bf3961e9928cba33
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433525"
---
# <a name="spropvalue"></a>SPropValue

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Descreve uma propriedade MAPI.
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapidefs. h  <br/> |
|Macros relacionadas:  <br/> |[CHANGE_PROP_TYPE](change_prop_type.md), [MVI_PROP](mvi_prop.md), [PROP_ID](prop_id.md), [PROP_TAG](prop_tag.md), [PROP_TYPE](prop_type.md) <br/> |
   
```cpp
typedef struct _SPropValue
{
  ULONG ulPropTag;
  ULONG dwAlignPad;
  union _PV Value;
} SPropValue, FAR *LPSPropValue;

```

## <a name="members"></a>Members

 **ulPropTag**
  
> Marca de propriedade da propriedade. As marcas de propriedade são inteiros não assinados de 32 bits que consistem no identificador exclusivo da propriedade nos 16 bits de ordem alta e no tipo da propriedade na ordem baixa de 16 bits.
    
 **dwAlignPad**
  
> Reservado para MAPI; Não use. 
    
 **Valor**
  
> União de valores de dados, o valor específico determinado pelo tipo de propriedade. A tabela a seguir lista para cada tipo de propriedade, o membro da União que deve ser usado e seu tipo de dados associado.
    
|**Tipo de propriedade**|**Valor**|**Tipo de dados do valor**|
|:-----|:-----|:-----|
|PT_I2 ou PT_SHORT  <br/> |**i** <br/> |short int  <br/> |
|PT_I4 ou PT_LONG (assinado)  <br/> |**Esq** <br/> |Longas  <br/> |
|PT_I4 ou PT_LONG (não assinado)  <br/> |**UL** <br/> |ULONG  <br/> |
|PT_R4 ou PT_FLOAT  <br/> |**FLT** <br/> |float  <br/> |
|PT_R8 ou PT_DOUBLE  <br/> |**ao duas vezes** <br/> |double  <br/> |
|PT_BOOLEAN  <br/> |**b** <br/> |int curto não assinado  <br/> |
|PT_CURRENCY  <br/> |**cur** <br/> |[CURRENCY](currency.md) <br/> |
|PT_APPTIME  <br/> |**por** <br/> |double  <br/> |
|PT_SYSTIME  <br/> |**ft** <br/> |[FILETIME](filetime.md) <br/> |
|PT_STRING8  <br/> |**lpszA** <br/> |LPSTR  <br/> |
|PT_BINARY  <br/> |**Bno** <br/> |BYTE [matriz]  <br/> |
|PT_UNICODE  <br/> |**lpszW** <br/> |LPWSTR  <br/> |
|PT_CLSID  <br/> |**lpguid** <br/> |LPGUID  <br/> |
|PT_I8 ou PT_LONGLONG  <br/> |**Li** <br/> |**LARGE_INTEGER** <br/> |
|PT_MV_I2  <br/> |**MVi** <br/> |[SShortArray](sshortarray.md) <br/> |
|PT_MV_LONG  <br/> |**MVI** <br/> |[SLongArray](slongarray.md) <br/> |
|PT_MV_R4  <br/> |**MVflt** <br/> |[SRealArray](srealarray.md) <br/> |
|PT_MV_DOUBLE  <br/> |**MVdbl** <br/> |[SDoubleArray](sdoublearray.md) <br/> |
|PT_MV_CURRENCY  <br/> |**MVcur** <br/> |[SCurrencyArray](scurrencyarray.md) <br/> |
|PT_MV_APPTIME  <br/> |**MVat** <br/> |[SAppTimeArray](sapptimearray.md) <br/> |
|PT_MV_SYSTIME  <br/> |**MVft** <br/> |[SDateTimeArray](sdatetimearray.md) <br/> |
|PT_MV_BINARY  <br/> |**MVbin** <br/> |[SBinaryArray](sbinaryarray.md) <br/> |
|PT_MV_STRING8  <br/> |**MVszA** <br/> |[SLPSTRArray](slpstrarray.md) <br/> |
|PT_MV_UNICODE  <br/> |**MVszW** <br/> |[SWStringArray](swstringarray.md) <br/> |
|PT_MV_CLSID  <br/> |**MVguid** <br/> |[SGuidArray](sguidarray.md) <br/> |
|PT_MV_I8  <br/> |**MVli** <br/> |[SLargeIntegerArray](slargeintegerarray.md) <br/> |
|PT_ERROR  <br/> |**err** <br/> |[SCODE](scode.md) <br/> |
|PT_NULL ou PT_OBJECT  <br/> |**x** <br/> |Longas  <br/> |
|PT_PTR  <br/> |**LPV** <br/> |Deixa\*  <br/> |
   
## <a name="remarks"></a>Comentários

O membro **ulPropTag** é composto de duas partes: 
  
- Um identificador na ordem alta de 16 bits.
    
- Um tipo na ordem baixa de 16 bits.
    
O identificador é um valor numérico dentro de um determinado intervalo. MAPI define intervalos para identificadores para descrever o que a propriedade é usada e quem é responsável por mantê-la. MAPI define restrições para cada uma das marcas de propriedade que ele suporta no arquivo de cabeçalho Mapitags. h.
  
O tipo indica o formato do valor da propriedade. MAPI define constantes para cada um dos tipos de propriedade que ele suporta no arquivo de cabeçalho mapidefs. h. 
  
Para obter uma lista completa dos intervalos de propriedades válidos para identificadores e tipos de propriedade, consulte o apêndice de [identificadores e tipos](property-identifiers-and-types.md) de propriedade. 
  
O membro **dwAlignPad** é usado como preenchimento para garantir o alinhamento correto nos computadores que exigem o alinhamento de 8 bytes para valores de 8 bytes. Os desenvolvedores que escrevem código nesses computadores devem usar rotinas de alocação de memória que alocam os arrays do **SPropValue** em limites de 8 bytes. 
  
Para obter mais informações, consulte [MAPI Property Type Overview](mapi-property-type-overview.md) e [atualizating MAPI Properties](updating-mapi-properties.md). 
  
## <a name="see-also"></a>Confira também



[Estruturas MAPI](mapi-structures.md)

