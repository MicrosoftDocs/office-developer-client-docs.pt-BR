---
title: attMAPIProps
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 806270c1-30e4-494e-9b03-7d1f2fc04099
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 185bfbb151c4f8d4e36b40b94393d14d50c33edf
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410452"
---
# <a name="attmapiprops"></a>attMAPIProps

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
O **atributo attMAPIProps** é especial porque pode ser usado para codificar qualquer propriedade MAPI que não tenha uma contraparte no conjunto de atributos definidos por TNEF existentes. Os dados do atributo são um conjunto contado de propriedades MAPI colocadas de ponta a ponta. O formato dessa codificação, que permite qualquer conjunto de propriedades MAPI, é o seguinte:  
  
 _Property_Seq:_
  
> contagem de  _Property_Value,..._
    
Deve haver tantas  _Property_Value_ itens como o valor de contagem de propriedades indica. 
  
 _Property_Value:_
  
> propriedade-tag _Property_property-tag  _Proptag_Name Property_
    
A marca de propriedade é simplesmente o valor associado ao identificador da propriedade, como 0x0037001F para **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)).
  
 _Propriedade:_
  
>  _Valor_ de contagem de  _valor,..._
    
 _Valor:_
  
> value-data value-size value-data padding value-size value-IID value-data padding
    
 _Proptag_Name:_
  
> name-guid name-kind name-id name-guid name-kind name-string-length name-string padding
    
O encapsulamento de cada propriedade varia com base no identificador da propriedade e no tipo de propriedade. Marcas de propriedade, identificadores e tipos são definidos nos arquivos de título Mapitags.h e Mapidefs.h.
  
Se a propriedade for uma propriedade nomeada, a marca da propriedade será imediatamente seguida pelo nome da propriedade MAPI, consistindo em um identificador global exclusivo (GUID), um tipo e um identificador ou uma cadeia de caracteres Unicode.
  
Propriedades e propriedades de valores múltiplos com valores de comprimento variável, como os tipos de propriedade PT_BINARY, PT_STRING8, PT_UNICODE ou PT_OBJECT, são tratadas da seguinte maneira. Primeiro, o número de valores, codificados como um longo sem sinal de 32 bits, é colocado no fluxo TNEF, seguido pelos valores individuais. Os dados de valor de cada propriedade são codificados como seu tamanho em bytes seguidos pelos dados de valor em si. Os dados de valor são adicionados a um limite de 4 byte, embora a quantidade de preenchimento não seja incluída no tamanho do valor.
  
Se a propriedade for do tipo PT_OBJECT, o tamanho do valor será seguido pelo identificador da interface do objeto. A implementação atual do TNEF suporta apenas os identificadores IID_IMessage, IID_IStorage e IID_Istream interface. O tamanho do identificador da interface está incluído no tamanho do valor.
  
Se o objeto for uma mensagem incorporada (ou seja, se ele tiver um tipo de propriedade de PT_OBJECT e um identificador de interface de IID_Imessage), os dados de valor serão codificados como um fluxo TNEF incorporado. A codificação real de uma mensagem incorporada na implementação do TNEF é feita abrindo um segundo objeto TNEF para o fluxo original e processando o fluxo embutido.
  

