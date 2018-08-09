---
title: Tipos de propriedades
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 71967150-1005-4c85-90f1-76fc7876c0d0
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: fd0f25f20c9e628a80d27f2b70e01dacc98229b7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770201"
---
# <a name="property-types"></a>Tipos de propriedades

  
  
**Aplica-se a**: Outlook 
  
MAPI suporta as propriedades de valor único e de valores múltiplos. Com uma propriedade de valor único, há um valor do tipo base da propriedade. Com uma propriedade de valores múltiplos, há vários valores do tipo base. 
  
Os tipos de valor único e vários valores de propriedade que ofereça suporte a MAPI são descritos na tabela a seguir. Para cada tipo de valor único que tem um tipo de vários valores correspondente, o tipo de valores múltiplos aparece entre parênteses após o tipo de valor único.
  
|**Tipo de propriedade**|**Valor hexadecimal**|**Descrição**|
|:-----|:-----|:-----|
|PT_UNSPECIFIED  <br/> |0000  <br/> |Indica que o tipo de propriedade é desconhecido. Esse tipo de propriedade é reservado para uso com os métodos de interface.  <br/> |
|PT_NULL  <br/> |0001  <br/> |Não indica que nenhum valor de propriedade. Esse tipo de propriedade é reservado para uso com os métodos de interface e que iguais a OLE digite VT_NULL.  <br/> |
|PT_I2 (PT_MV_I2)  <br/> |0002  <br/> |Inteiro assinado de (2 bytes) de 16 bits. Esse tipo de propriedade é o mesmo PT_SHORT (PT_MV_SHORT) e o OLE digite VT_I2.  <br/> |
|PT_I4 (PT_MV_I4)  <br/> |0003  <br/> |32 bits (4 bytes) inteiro com sinal ou. Esse tipo de propriedade é o mesmo PT_LONG (PT_MV_LONG) e o OLE digite VT_I4.  <br/> |
|PT_FLOAT (PT_MV_FLOAT)  <br/> |0004  <br/> |valor de ponto flutuante (8 bytes) de 32 bits. Esse tipo de propriedade é o mesmo que PT_R4 (PT_MV_R4) e o tipo OLE VT_R4.  <br/> |
|PT_DOUBLE (PT_MV_DOUBLE)  <br/> |0005  <br/> |valor de ponto flutuante (8 bytes) de 64 bits. Esse tipo de propriedade é o mesmo que PT_R8 e os tipos OLE VT_R8 e VT_DOUBLE.  <br/> |
|PT_CURRENCY (PT_MV_CURRENCY)  <br/> |0006  <br/> |64 bits (8 bytes) inteiro interpretada como decimal. Esse tipo de propriedade é compatível com o tipo de moeda do Microsoft Visual Basic e é que o mesmo que o OLE digitar VT_CY.  <br/> |
|PT_APPTIME (PT_MV_APPTIME)  <br/> |0007  <br/> |Valor Double que será interpretado como a data e hora. A parte inteira é a data e a parte de fração é a hora. Esse tipo de propriedade é o mesmo que o tipo OLE VT_DATE e é compatível com a representação de tempo do Microsoft Visual Basic.  <br/> |
|PT_ERROR  <br/> |000A  <br/> |Valor SCODE; inteiro não assinado de (4 bytes) de 32 bits. Esse tipo de propriedade é o mesmo que o tipo OLE VT_ERROR.  <br/> |
|PT_BOOLEAN (PT_MV_12)  <br/> |000B  <br/> |16 bits (2 bytes) booleano valor onde o zero é igual a **Falso** e é de diferente de zero igual a **true**. Esse tipo de propriedade é o mesmo que o tipo OLE VT_BOOL.  <br/> |
|PT_OBJECT  <br/> |000D  <br/> |Ponteiro para um objeto que implementa a interface **IUnknown** . Esse tipo de propriedade é semelhante a vários tipos de OLE como VT_UNKNOWN.  <br/> |
|PT_I8 (PT_MV_I8)  <br/> |0014  <br/> |64 bits (8 bytes) inteiro com sinal ou que usa a estrutura **LARGE_INTEGER** . Esse tipo de propriedade é o mesmo como PT_I8 e o OLE tipo VT_I8.  <br/> |
|PT_STRING8 (PT_MV_STRING8)  <br/> |001E  <br/> |Cadeia de caracteres de (2 bytes) de 8 bits terminada em nulo. Esse tipo de propriedade é o mesmo que o tipo OLE VT_LPSTR.  <br/> |
|PT_TSTRING (PT_MV_TSTRING)  <br/> |001F  <br/> |Cadeia de caracteres de (2 bytes) de 16 bits terminada em nulo. Propriedades com esse tipo de tem o tipo de propriedade redefinir PT_UNICODE ao compilar com o símbolo UNICODE e PT_STRING8 ao compilar não com o símbolo UNICODE. Esse tipo de propriedade é o mesmo tipo OLE VT_LPSTR para propriedades de PT_STRING8 resultantes e VT_LPWSTR para propriedades PT_UNICODE  <br/> |
|PT_SYSTIME (PT_MV_SYSTIME)  <br/> |0040  <br/> |valor inteiro de (8 bytes) de 64 bits de data e hora na forma de uma estrutura **FILETIME** . Esse tipo de propriedade é o mesmo que o tipo OLE VT_FILETIME.  <br/> |
|PT_CLSID (PT_MV_CLSID)  <br/> |0048  <br/> |Valor de estrutura **CLSID** . Esse tipo de propriedade é o mesmo que o tipo OLE VT_CLSID.  <br/> |
|PT_SVREID  <br/> |00FB  <br/> |Tamanho variável, uma 16 bits (2 bytes) **contagem** seguido por uma estrutura.  <br/> |
|PT_SRESTRICT  <br/> |00FD  <br/> |Tamanho variável, uma matriz de bytes representando uma ou mais estruturas de restrição.  <br/> |
|PT_ACTIONS  <br/> |00FE  <br/> |Tamanho variável, uma de 16 bits (2 bytes) **contagem** de ações (não bytes) seguido pelo que muitas estruturas de ação de regra.  <br/> |
|PT_BINARY (PT_MV_BINARY)  <br/> |0102  <br/> |Valor de estrutura **SBinary** , uma matriz de bytes contado.  <br/> |
   
> [!NOTE]
> Para determinar o valor Hex para o tipo de propriedade de valores múltiplos, ou o PT_MV tipo de sinalizador (0x00001000) para o valor da propriedade Hex. Por exemplo, o valor Hex PT_MV_UNICODE é 0x101F e o valor Hex PT_MV_BINARY é 0x1102. 
  

