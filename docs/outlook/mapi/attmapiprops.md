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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32318120"
---
# <a name="attmapiprops"></a>attMAPIProps

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
O atributo **attMAPIProps** é especial, pois pode ser usado para codificar qualquer propriedade MAPI que não tenha uma contraparte no conjunto de atributos definidos por TNEF existentes. Os dados de atributo são um conjunto contado de propriedades MAPI dispostos de ponta a ponta. O formato dessa codificação, que permite qualquer conjunto de propriedades MAPI, é o seguinte:  
  
 _Property_Seq:_
  
> Propriedade-contagem _Property_Value,..._
    
Deve haver tantos itens de _Property_Value_ quanto o valor de Property-Count indica. 
  
 _Property_Value:_
  
> Propriedade-tag _Property_property-tag _Proptag_Name Property_
    
A marca de propriedade é simplesmente o valor associado ao identificador de propriedade, como 0x0037001F para **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)).
  
 _Propriedades_
  
>  __ Valor valor-contagem valor _,..._
    
 _Valor:_
  
> valor-valor de dados-tamanho valor-valor do preenchimento valor-valor de IID-enchimento dos dados
    
 _Proptag_Name:_
  
> name-GUID Name-Kind Name-nome do ID-nome do tipo-tipo nome-cadeia de caracteres-enchimento da cadeia de caracteres
    
O encapsulamento de cada propriedade varia de acordo com o identificador de propriedade e o tipo de propriedade. Marcas de propriedade, identificadores e tipos são definidos nos arquivos de cabeçalho Mapitags. h e mapidefs. h.
  
Se a propriedade for uma propriedade nomeada, a marca de propriedade será imediatamente seguida pelo nome da propriedade MAPI, consistindo em um identificador global exclusivo (GUID), um tipo e um identificador ou uma cadeia de caracteres Unicode.
  
Propriedades e propriedades de vários valores com valores de comprimento variável, como os tipos de propriedade PT_BINARY, PT_STRING8, PT_UNICODE ou PT_OBJECT, são tratados da seguinte maneira. Primeiro, o número de valores, codificado como um Long de 32 bits não assinado, é colocado no fluxo TNEF, seguido pelos valores individuais. Os dados de valor de cada propriedade são codificados como seu tamanho em bytes seguidos pelo valor-dados propriamente dito. O valor-dados é preenchido para um limite de 4 bytes, embora a quantidade de enchimento não seja incluída no tamanho do valor.
  
Se a propriedade for do tipo PT_OBJECT, o tamanho de valor será seguido pelo identificador de interface do objeto. A implementação atual do TNEF só oferece suporte aos identificadores de interface IID_IMessage, IID_IStorage e IID_Istream. O tamanho do identificador de interface é incluído no tamanho do valor.
  
Se o objeto for uma mensagem incorporada (ou seja, tiver um tipo de propriedade de PT_OBJECT e um identificador de interface de IID_Imessage), os dados de valor serão codificados como um fluxo TNEF incorporado. A codificação real de uma mensagem incorporada na implementação do TNEF é feita abrindo um segundo objeto TNEF para o fluxo original e processando o fluxo em linha.
  

