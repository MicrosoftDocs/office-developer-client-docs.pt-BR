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
ms.openlocfilehash: 60528162917a8a383060adbcadefb610aa42ce32
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22580968"
---
# <a name="spropvalue"></a>SPropValue

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Descreve uma propriedade MAPI.
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapidefs.h  <br/> |
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
  
> Marca de propriedade para a propriedade. As marcas de propriedade são números inteiros não assinados de 32 bits consistindo a identificador exclusivo da propriedade nos 16 bits superiores e o tipo da propriedade nos ordem baixa 16 bits.
    
 **dwAlignPad**
  
> Reservado para MAPI; Não use. 
    
 **Valor**
  
> União de valores de dados, o valor específico determinado pelo tipo de propriedade. A tabela a seguir lista para cada tipo de propriedade, o membro da união que deverão ser usada e seu tipo de dados associados.
    
|**Tipo de propriedade**|**Valor**|**Tipo de dados de valor**|
|:-----|:-----|:-----|
|PT_I2 ou PT_SHORT  <br/> |**Eu** <br/> |short int  <br/> |
|PT_I4 ou PT_LONG (conectado)  <br/> |**l** <br/> |Longas  <br/> |
|PT_I4 ou PT_LONG (sem sinal)  <br/> |**UL** <br/> |ULONG  <br/> |
|PT_R4 ou PT_FLOAT  <br/> |**especificados devem receber** <br/> |float  <br/> |
|PT_R8 ou PT_DOUBLE  <br/> |**duplo** <br/> |double  <br/> |
|PT_BOOLEAN  <br/> |**b** <br/> |int curto não assinado  <br/> |
|PT_CURRENCY  <br/> |**atual** <br/> |[CURRENCY](currency.md) <br/> |
|PT_APPTIME  <br/> |**em** <br/> |double  <br/> |
|PT_SYSTIME  <br/> |**FT** <br/> |[FILETIME](filetime.md) <br/> |
|PT_STRING8  <br/> |**lpszA** <br/> |LPSTR  <br/> |
|PT_BINARY  <br/> |**bin** <br/> |BYTE [matriz]  <br/> |
|PT_UNICODE  <br/> |**lpszW** <br/> |LPWSTR  <br/> |
|PT_CLSID  <br/> |**lpguid** <br/> |LPGUID  <br/> |
|PT_I8 ou PT_LONGLONG  <br/> |**li** <br/> |**LARGE_INTEGER** <br/> |
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
|PT_PTR  <br/> |**lpv** <br/> |VOID\*  <br/> |
   
## <a name="remarks"></a>Comentários

O membro **ulPropTag** é composto por duas partes: 
  
- Um identificador nos superiores 16 bits.
    
- Um tipo nos ordem baixa 16 bits.
    
O identificador é um valor numérico dentro de um determinado intervalo. MAPI define os intervalos para os identificadores descrever o que a propriedade é usada para e quem é responsável por manter a ele. MAPI define restrições para cada um das marcas de propriedade ao qual ele oferece suporte no arquivo de cabeçalho Mapitags.h.
  
O tipo indica o formato para o valor da propriedade. MAPI define as constantes para cada um dos tipos de propriedade que ele suporta no arquivo de cabeçalho Mapidefs.h. 
  
Para obter uma lista completa dos intervalos de propriedade válidos para tipos de propriedade e identificadores, consulte o Apêndice [tipos e identificadores de propriedade](property-identifiers-and-types.md) . 
  
O membro **dwAlignPad** é usado como preenchimento para tornar o alinhamento adequado claro que em computadores que exijam o alinhamento de 8 bytes para valores de 8 bytes. Os desenvolvedores que escrever código nesses computadores devem usar rotinas de alocação de memória que alocar as matrizes **SPropValue** nos limites de 8 bytes. 
  
Para obter mais informações, consulte [Visão geral do tipo de propriedade de MAPI](mapi-property-type-overview.md) e [Atualizar propriedades de MAPI](updating-mapi-properties.md). 
  
## <a name="see-also"></a>Confira também



[Estruturas MAPI](mapi-structures.md)

