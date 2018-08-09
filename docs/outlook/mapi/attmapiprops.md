---
title: attMAPIProps
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 806270c1-30e4-494e-9b03-7d1f2fc04099
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: eef480e8b024565ab282fb242a36336cd17384a1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766198"
---
# <a name="attmapiprops"></a>attMAPIProps

  
  
**Aplica-se a**: Outlook 
  
O atributo **attMAPIProps** é especial ele pode ser usado para codificar qualquer propriedade MAPI que não tem um equivalente no conjunto de atributos definidos pelo TNEF existentes. Os dados de atributo são um conjunto contado das propriedades MAPI formatado de ponta a ponta. O formato dessa codificação, que permite a qualquer conjunto de propriedades MAPI, é o seguinte:  
  
 _Property_Seq:_
  
> Contagem de propriedade _Property_Value,..._
    
Deve haver quantos itens _Property_Value_ indica o valor de contagem de propriedade. 
  
 _Property_Value:_
  
> marca a propriedade tag-_Property_property _Propriedade Proptag_Name_
    
A marca de propriedade é simplesmente o valor associado com o identificador de propriedade, como 0x0037001F para **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)).
  
 _Propriedade:_
  
>  Valor-contagem de _valor_ _valor,..._
    
 _Valor:_
  
> tamanho do valor de dados do valor valor-dados preenchimento de dados do valor do tamanho do valor valor-IID de preenchimento
    
 _Proptag_Name:_
  
> preenchimento de cadeia de caracteres de nome de comprimento da cadeia de caracteres de nome do guid de nome nome-guid de id de nome de tipo de nome tipo de nome
    
O encapsulamento de cada propriedade varia de acordo com o identificador de propriedade e o tipo de propriedade. Tipos e identificadores de marcas de propriedade são definidos nos arquivos de cabeçalho Mapitags.h e Mapidefs.h.
  
Se a propriedade for uma propriedade com nome, a marca de propriedade é imediatamente seguida pelo nome da propriedade MAPI, consistindo em um identificador global exclusivo (GUID), um tipo e um identificador ou uma cadeia de caracteres Unicode.
  
Vários valores de propriedades e valores de comprimento variável, como os tipos de propriedade PT_BINARY, PT_STRING8, PT_UNICODE ou PT_OBJECT, são tratados da seguinte maneira. Primeiro o número de valores, codificadas como de 32 bits não assinados longas é colocado no stream TNEF, seguido por valores individuais. Dados do valor de cada propriedade é codificado como seu tamanho em bytes, seguido dos dados de valor em si. Os dados do valor é preenchido a um limite de 4 bytes, embora a quantidade de preenchimento não está incluída no tamanho do valor.
  
Se a propriedade for do tipo PT_OBJECT, o tamanho do valor é seguido pelo identificador de interface do objeto. A implementação atual do TNEF suporta apenas os identificadores de interface IID_IMessage, IID_IStorage e IID_Istream. O tamanho do identificador de interface é incluído no valor-tamanho.
  
Se o objeto for uma mensagem incorporada (ou seja, tem um tipo de propriedade de PT_OBJECT e um identificador de interface de IID_Imessage), os dados do valor são codificados como um fluxo TNEF incorporado. A codificação real de uma mensagem incorporada na implementação de TNEF é feita abrindo um segundo objeto TNEF para o fluxo de original e o embutido de fluxo de processamento.
  

