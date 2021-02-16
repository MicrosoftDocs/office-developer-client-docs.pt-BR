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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407050"
---
# <a name="property-types"></a>Tipos de propriedade

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
MAPI supports both single-value and multiple-value properties. Com uma propriedade de valor único, há um valor do tipo base para a propriedade. Com uma propriedade de vários valores, há vários valores do tipo base. 
  
Os tipos de propriedade de valor único e de vários valores que o MAPI suporta são descritos na tabela a seguir. Para cada tipo de valor único que tenha um tipo de vários valores correspondente, o tipo de vários valores aparece entre parênteses após o tipo de valor único.
  
|**Tipo de Propriedade**|**Valor hexadecimal**|**Descrição**|
|:-----|:-----|:-----|
|PT_UNSPECIFIED  <br/> |0000  <br/> |Indica que o tipo de propriedade é desconhecido. Esse tipo de propriedade é reservado para uso com métodos de interface.  <br/> |
|PT_NULL  <br/> |0001  <br/> |Indica nenhum valor de propriedade. Esse tipo de propriedade é reservado para uso com métodos de interface e é o mesmo que o tipo OLE VT_NULL.  <br/> |
|PT_I2 (PT_MV_I2)  <br/> |0002  <br/> |Inteiro de 16 bits (2 byte) assinado. Esse tipo de propriedade é o mesmo PT_SHORT (PT_MV_SHORT) e o tipo OLE VT_I2.  <br/> |
|PT_I4 (PT_MV_I4)  <br/> |0003  <br/> |Inteiro de 32 bits (4 byte) assinado ou não assinado. Esse tipo de propriedade é o mesmo PT_LONG (PT_MV_LONG) e o tipo OLE VT_I4.  <br/> |
|PT_FLOAT (PT_MV_FLOAT)  <br/> |0004  <br/> |Valor de ponto flutuante de 32 bits (8 byte). Esse tipo de propriedade é o mesmo PT_R4 (PT_MV_R4) e o tipo OLE VT_R4.  <br/> |
|PT_DOUBLE (PT_MV_DOUBLE)  <br/> |0005  <br/> |Valor de ponto flutuante de 64 bits (8 byte). Esse tipo de propriedade é o mesmo PT_R8 e os tipos OLE VT_R8 e VT_DOUBLE.  <br/> |
|PT_CURRENCY (PT_MV_CURRENCY)  <br/> |0006  <br/> |Inteiro de 64 bits (8 byte) interpretado como decimal. Esse tipo de propriedade é compatível com o tipo currency do Microsoft Visual Basic e é o mesmo que o tipo OLE VT_CY.  <br/> |
|PT_APPTIME (PT_MV_APPTIME)  <br/> |0007  <br/> |Valor duplo que é interpretado como data e hora. A parte inteira é a data e a parte fracionada é a hora. Esse tipo de propriedade é o mesmo que o tipo OLE VT_DATE e é compatível com a representação de hora do Microsoft Visual Basic.  <br/> |
|PT_ERROR  <br/> |000A  <br/> |Valor de SCODE; Inteiro não assinado de 32 bits (4 byte). Esse tipo de propriedade é igual ao tipo OLE VT_ERROR.  <br/> |
|PT_BOOLEAN (PT_MV_12)  <br/> |000B  <br/> |Valor booleano de 16 bits (2 byte), onde zero é igual a **falso** e diferente de zero é igual a **true**. Esse tipo de propriedade é igual ao tipo OLE VT_BOOL.  <br/> |
|PT_OBJECT  <br/> |000D  <br/> |Ponteiro para um objeto que implementa a interface **IUnknown.** Esse tipo de propriedade é semelhante a vários tipos OLE, como VT_UNKNOWN.  <br/> |
|PT_I8 (PT_MV_I8)  <br/> |0014  <br/> |Inteiro assinado ou não assinado de 64 bits (8 byte) que usa a **estrutura LARGE_INTEGER** assinatura. Esse tipo de propriedade é o mesmo PT_I8 e o tipo OLE VT_I8.  <br/> |
|PT_STRING8 (PT_MV_STRING8)  <br/> |001E  <br/> |Cadeia de caracteres terminada por 8 bits (2 byte) terminada por caractere nulo. Esse tipo de propriedade é igual ao tipo OLE VT_LPSTR.  <br/> |
|PT_TSTRING (PT_MV_TSTRING)  <br/> |001F  <br/> |Cadeia de caracteres terminada por 16 bits (2 byte) terminada por caractere nulo. Propriedades com esse tipo têm o tipo de propriedade redefinido como PT_UNICODE quando compiladas com o símbolo UNICODE e para PT_STRING8 quando não estiver compilando com o símbolo UNICODE. Esse tipo de propriedade é o mesmo que o tipo OLE VT_LPSTR para propriedades PT_STRING8 resultantes e VT_LPWSTR propriedades PT_UNICODE propriedades  <br/> |
|PT_SYSTIME (PT_MV_SYSTIME)  <br/> |0040  <br/> |Dados inteiros de 64 bits (8 byte) e valor de hora na forma de uma **estrutura FILETIME.** Esse tipo de propriedade é igual ao tipo OLE VT_FILETIME.  <br/> |
|PT_CLSID (PT_MV_CLSID)  <br/> |0048  <br/> |**Valor da estrutura CLSID.** Esse tipo de propriedade é igual ao tipo OLE VT_CLSID.  <br/> |
|PT_SVREID  <br/> |00FB  <br/> |Tamanho da variável, um **COUNT** de 16 bits (2 byte) seguido por uma estrutura.  <br/> |
|PT_SRESTRICT  <br/> |00FD  <br/> |Tamanho da variável, uma matriz de byte que representa uma ou mais estruturas de restrição.  <br/> |
|PT_ACTIONS  <br/> |00FE  <br/> |Tamanho da variável, uma **CONTAGEM** de 16 bits (2 bytes) de ações (não bytes) seguida por muitas estruturas de Ação de Regra.  <br/> |
|PT_BINARY (PT_MV_BINARY)  <br/> |0102  <br/> |**Valor da estrutura SBinary,** uma matriz de byte contada.  <br/> |
   
> [!NOTE]
> Para determinar o valor Hex para o tipo de propriedade de vários valores, OU o sinalizador PT_MV (0x00001000) para o valor Hex para o tipo de propriedade. Por exemplo, o valor hexaxa para PT_MV_UNICODE é 0x101F e o valor hexaxa para PT_MV_BINARY é 0x1102. 
  

