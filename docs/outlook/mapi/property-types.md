---
title: Tipos de propriedade
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 71967150-1005-4c85-90f1-76fc7876c0d0
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 43b0090192a2f9b02acee4edf471c5ae6c6de7e8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328487"
---
# <a name="property-types"></a>Tipos de propriedade

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
O MAPI oferece suporte a propriedades de valor único e de valores múltiplos. Com uma propriedade de valor único, há um valor do tipo base para a propriedade. Com uma propriedade de vários valores, há vários valores de tipo base. 
  
Os tipos de propriedade de valor único e de vários valores que o MAPI suporta são descritos na tabela a seguir. Para cada tipo de valor único que tem um tipo de vários valores correspondente, o tipo de vários valores aparece entre parênteses após o tipo de valor único.
  
|**Tipo de Propriedade**|**Valor hexadecimal**|**Descrição**|
|:-----|:-----|:-----|
|PT_UNSPECIFIED  <br/> |0000  <br/> |Indica que o tipo de propriedade é desconhecido. Esse tipo de propriedade é reservado para uso com métodos de interface.  <br/> |
|PT_NULL  <br/> |0001  <br/> |Indica nenhum valor de propriedade. Esse tipo de propriedade é reservado para uso com métodos de interface e é o mesmo que o tipo de OLE VT_NULL.  <br/> |
|PT_I2 (PT_MV_I2)  <br/> |0002  <br/> |Inteiro assinado de 16 bits (2 bytes). Esse tipo de propriedade é o mesmo que PT_SHORT (PT_MV_SHORT) e o tipo de OLE VT_I2.  <br/> |
|PT_I4 (PT_MV_I4)  <br/> |0003  <br/> |Um inteiro assinado ou não assinado de 32 bits (4 bytes). Esse tipo de propriedade é o mesmo que PT_LONG (PT_MV_LONG) e o tipo de OLE VT_I4.  <br/> |
|PT_FLOAT (PT_MV_FLOAT)  <br/> |0004  <br/> |valor de ponto flutuante de 32 bits (8 bytes). Esse tipo de propriedade é o mesmo que PT_R4 (PT_MV_R4) e o tipo de OLE VT_R4.  <br/> |
|PT_DOUBLE (PT_MV_DOUBLE)  <br/> |0005  <br/> |valor de ponto flutuante de 64 bits (8 bytes). Esse tipo de propriedade é o mesmo que PT_R8 e os tipos de OLE VT_R8 e VT_DOUBLE.  <br/> |
|PT_CURRENCY (PT_MV_CURRENCY)  <br/> |0006  <br/> |número inteiro de 64 bits (8 bytes) interpretado como Decimal. Esse tipo de propriedade é compatível com o tipo de moeda Microsoft Visual Basic e é o mesmo que o tipo de OLE VT_CY.  <br/> |
|PT_APPTIME (PT_MV_APPTIME)  <br/> |0007  <br/> |Valor Double que é interpretado como data e hora. A parte inteira é a data e a parte fracionária é a hora. Esse tipo de propriedade é o mesmo que o tipo de OLE VT_DATE e é compatível com a representação de tempo do Microsoft Visual Basic.  <br/> |
|PT_ERROR  <br/> |000A  <br/> |Valor SCODE; 32 bits (4 bytes) inteiro não assinado. Esse tipo de propriedade é o mesmo que o tipo de OLE VT_ERROR.  <br/> |
|PT_BOOLEAN (PT_MV_12)  <br/> |000B  <br/> |valor booliano de 16 bits (2 bytes) onde zero é igual a **falso** e diferente de zero é igual a **true**. Esse tipo de propriedade é o mesmo que o tipo de OLE VT_BOOL.  <br/> |
|PT_OBJECT  <br/> |000D  <br/> |Ponteiro para um objeto que implementa a interface **IUnknown** . Esse tipo de propriedade é semelhante a vários tipos de OLE, como VT_UNKNOWN.  <br/> |
|PT_I8 (PT_MV_I8)  <br/> |0014  <br/> |Um inteiro assinado ou sem sinal de 64 bits (8 bytes) que usa a estrutura **LARGE_INTEGER** . Esse tipo de propriedade é o mesmo que PT_I8 e o tipo de OLE VT_I8.  <br/> |
|PT_STRING8 (PT_MV_STRING8)  <br/> |001E  <br/> |Sequência de caracteres de 8 bits (2 bytes) terminada em nulo. Esse tipo de propriedade é o mesmo que o tipo de OLE VT_LPSTR.  <br/> |
|PT_TSTRING (PT_MV_TSTRING)  <br/> |001F  <br/> |Cadeia de caracteres de 16 bits (2 bytes) terminada em nulo. Propriedades com esse tipo têm o tipo de propriedade reset como PT_UNICODE ao compilar com o símbolo UNICODE e como PT_STRING8 quando não estiver Compilando com o símbolo UNICODE. Esse tipo de propriedade é o mesmo que o tipo de OLE VT_LPSTR para propriedades de PT_STRING8 resultantes e VT_LPWSTR para propriedades de PT_UNICODE  <br/> |
|PT_SYSTIME (PT_MV_SYSTIME)  <br/> |0040  <br/> |dados inteiros de 64 bits (8 bytes) e o valor de tempo na forma de uma estrutura **FILETIME** . Esse tipo de propriedade é o mesmo que o tipo de OLE VT_FILETIME.  <br/> |
|PT_CLSID (PT_MV_CLSID)  <br/> |0048  <br/> |Valor da estrutura **CLSID** . Esse tipo de propriedade é o mesmo que o tipo de OLE VT_CLSID.  <br/> |
|PT_SVREID  <br/> |00FB  <br/> |Tamanho variável, uma **contagem** de 16 bits (2 bytes) seguida de uma estrutura.  <br/> |
|PT_SRESTRICT  <br/> |00FD  <br/> |Tamanho da variável, uma matriz de bytes representando uma ou mais estruturas de restrição.  <br/> |
|PT_ACTIONS  <br/> |00FE  <br/> |Tamanho variável, uma **contagem** de ações de 16 bits (de 2 bytes) (não bytes) seguidas por várias estruturas de ação de regra.  <br/> |
|PT_BINARY (PT_MV_BINARY)  <br/> |0102  <br/> |O valor da estrutura **SBinary** , uma matriz de bytes contada.  <br/> |
   
> [!NOTE]
> Para determinar o valor hex para o tipo de propriedade de vários valores, ou o sinalizador PT_MV (0x00001000) para o valor hex do tipo de propriedade. Por exemplo, o valor hex de PT_MV_UNICODE é 0x101F e o valor hex de PT_MV_BINARY é 0x1102. 
  

