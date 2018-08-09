---
title: Sintaxe do fluxo de TNEF
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 1353d494-c266-4715-afe7-14543a1bbe1b
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: cbaf37415608dd1d79a06be65b34632f2b4afc89
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770625"
---
# <a name="tnef-stream-syntax"></a>Sintaxe do fluxo de TNEF

  
  
**Aplica-se a**: Outlook 
  
Este tópico apresenta uma Bakus-Nauer como a descrição da sintaxe TNEF stream. Nesta descrição, elementos não terminais que têm uma definição mais estão em itálico. Constantes e literais itens estão em negrito. Sequências de elementos são listadas na ordem em uma única linha. Por exemplo, o item de _fluxo_ consiste a constante **TNEF_SIGNATURE**, seguido por uma _chave_, seguido por um _objeto_. Quando um item tem mais de uma implementação possível, as alternativas são listadas em linhas consecutivas. Por exemplo, um _objeto_ pode consistir em um _Message_Seq_, _Message_Seq_ seguido por um _Attach_Seq_ou apenas um _Attach_Seq_.
  
 _TNEF_Stream:_
  
> **TNEF_SIGNATURE** _Chave_ _Objeto_
    
 _Chave:_
  
> um inteiro não assinado de 16 bits diferente de zero
    
Transportes TNEF habilitado para geram esse valor antes de usar a implementação de TNEF para gerar um fluxo TNEF.
  
 _Objeto:_
  
>  _Message_Seq Message_Seq Attach_Seq Attach_Seq_
    
 _Message_Seq:_
  
>  _attTnefVersion attTnefVersion Msg_Attribute_Seq attTnefVersion attMessageClass attTnefVersion attMessageClass Msg_Attribute_Seq attMessageClass attMessageClass Msg_Attribute_Seq Msg_Attribute_Seq_
    
 _attTnefVersion:_
  
> **LVL_MESSAGE attTnefVersion sizeof(ULONG)** soma de verificação **0x00010000** 
    
 _attMessageClass:_
  
> **LVL_MESSAGE attMessageClass** soma de verificação de _msg_class_length msg_class_ 
    
 _Msg_Attribute_Seq:_
  
>  _Msg_Attribute Msg_Attribute Msg_Attribute_Seq_
    
 _Msg_Attribute:_
  
> Soma de verificação de dados de atributo do **LVL_MESSAGE** ID do atributo comprimento do atributo 
    
ID do atributo é um dos identificadores de atributo TNEF, como **attSubject**. Comprimento do atributo é o tamanho em bytes dos dados de atributo. Dados de atributo são os dados associados com o atributo.
  
 _Attach_Seq:_
  
>  _attRenddata attRenddata Att_Attribute_Seq_
    
 _attRenddata:_
  
> **LVL_ATTACHMENT attRenddata** soma de verificação de renddata **sizeof(RENDDATA)** 
    
Renddata é os dados associados a estrutura **RENDDATA** que contém as informações de renderização do anexo correspondente. A estrutura **RENDDATA** é definida no TNEF. Arquivo de cabeçalho H. 
  
 _Att_Attribute_Seq:_
  
>  _Att_Attribute Att_Attribute Att_Attribute_Seq_
    
 _Att_Attribute:_
  
> Soma de verificação de dados de atributo do **LVL_ATTACHMENT** ID do atributo comprimento do atributo 
    
ID do atributo, comprimento de atributo e dados de atributo têm os significados mesmos que para o item Msg_Attribute.
  

