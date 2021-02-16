---
title: Sintaxe de fluxo TNEF
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 1353d494-c266-4715-afe7-14543a1bbe1b
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 12d2a92ff80897456707c7ab8af8f704605c85d0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423024"
---
# <a name="tnef-stream-syntax"></a>Sintaxe de fluxo TNEF

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Este tópico apresenta uma Bakus-Nauer como a descrição da sintaxe de fluxo TNEF. Nesta descrição, os elementos não modernos que têm uma definição posterior estão em itálico. Constantes e itens literais estão em negrito. Sequências de elementos são listadas em ordem em uma única linha. For example, the  _Stream_ item consists of the constant **TNEF_SIGNATURE**, followed by a  _Key_, followed by an  _Object_. Quando um item tem mais de uma implementação possível, as alternativas são listadas em linhas consecutivas. Por exemplo, um  _objeto_ pode consistir em um  _Message_Seq_, um  _Message_Seq_ seguido por um  _Attach_Seq_ ou apenas um  _Attach_Seq_.
  
 _TNEF_Stream:_
  
> **TNEF_SIGNATURE** _chave do_ _objeto_
    
 _Chave:_
  
> um inteiro não assinado de 16 bits diferente de zero
    
Os transporte habilitados para TNEF geram esse valor antes de usar a implementação do TNEF para gerar um fluxo TNEF.
  
 _Objeto:_
  
>  _Message_Seq Message_Seq Attach_Seq Attach_Seq_
    
 _Message_Seq:_
  
>  _attTnefVersion attTnefVersion Msg_Attribute_Seq attTnefVersion attMessageClass attTnefVersion attMessageClass Msg_Attribute_Seq attMessageClass attMessageClass Msg_Attribute_Seq Msg_Attribute_Seq_
    
 _attTnefVersion:_
  
> **LVL_MESSAGE tamanho de attTnefVersion (ULONG)** 0x00010000 **verificação** 
    
 _attMessageClass:_
  
> **LVL_MESSAGE attMessageClass** _msg_class_length msg_class_ verificação 
    
 _Msg_Attribute_Seq:_
  
>  _Msg_Attribute Msg_Attribute Msg_Attribute_Seq_
    
 _Msg_Attribute:_
  
> **LVL_MESSAGE** verificação atributo-ID atributo-length attribute-data 
    
Attribute-ID é um dos identificadores de atributo TNEF, como **attSubject**. Comprimento do atributo é o comprimento em bytes dos dados do atributo. Dados de atributo são os dados associados ao atributo.
  
 _Attach_Seq:_
  
>  _attRenddata attRenddata Att_Attribute_Seq_
    
 _attRenddata:_
  
> **LVL_ATTACHMENT verificação de renddata attRenddata** **sizeof (RENDDATA)** 
    
Os renddata são os dados associados à estrutura **RENDDATA** que contém as informações de renderização do anexo correspondente. A **estrutura RENDDATA** é definida no TNEF. Arquivo de header H. 
  
 _Att_Attribute_Seq:_
  
>  _Att_Attribute Att_Attribute Att_Attribute_Seq_
    
 _Att_Attribute:_
  
> **LVL_ATTACHMENT** verificação atributo-ID atributo-length attribute-data 
    
Attribute-ID, attribute-length, and attribute-data have the same meanings as for the Msg_Attribute item.
  

