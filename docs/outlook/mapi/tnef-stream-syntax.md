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
  
Este tópico apresenta um Bakus-Nauer como a descrição da sintaxe de fluxo TNEF. Nesta descrição, os elementos não terminais que têm uma definição adicional estão em itálico. Constantes e itens literais estão em negrito. As sequências de elementos são listadas em ordem em uma única linha. Por exemplo, o item _Stream_ consiste na constante **TNEF_SIGNATURE**, seguida por uma _chave_, seguida por um _objeto_. Quando um item tem mais de uma implementação possível, as alternativas são listadas em linhas consecutivas. Por exemplo, um _objeto_ pode consistir em um _Message_Seq_, um _Message_Seq_ seguido por um _Attach_Seq_ou apenas um _Attach_Seq_.
  
 _TNEF_Stream:_
  
> **TNEF_SIGNATURE** _Chave_ _Objeto_
    
 _Chaves_
  
> um inteiro não assinado de 16 bits diferente de zero
    
Os transportes habilitados para TNEF geram esse valor antes de usar a implementação TNEF para gerar um fluxo TNEF.
  
 _Objeções_
  
>  _Message_Seq Message_Seq Attach_Seq Attach_Seq_
    
 _Message_Seq:_
  
>  _attTnefVersion attTnefVersion Msg_Attribute_Seq attTnefVersion attMessageClass attTnefVersion attMessageClass Msg_Attribute_Seq attMessageClass attMessageClass Msg_Attribute_Seq Msg_Attribute_Seq_
    
 _attTnefVersion:_
  
> **LVL_MESSAGE attTnefVersion sizeof (ULong)** soma de verificação **0x00010000** 
    
 _attMessageClass:_
  
> **LVL_MESSAGE attMessageClass** _msg_class_length msg_class_ de soma de verificação 
    
 _Msg_Attribute_Seq:_
  
>  _Msg_Attribute Msg_Attribute Msg_Attribute_Seq_
    
 _Msg_Attribute:_
  
> Atributo **LVL_MESSAGE** -atributo de ID-soma de verificação de dados 
    
Attribute-ID é um dos identificadores de atributo TNEF, como **attSubject**. Attribute-length é o tamanho em bytes dos dados de atributo. O atributo-data é os dados associados ao atributo.
  
 _Attach_Seq:_
  
>  _attRenddata attRenddata Att_Attribute_Seq_
    
 _attRenddata:_
  
> **LVL_ATTACHMENT attRenddata** RENDDATA **de soma de verificação de sizeof (RENDDATA)** 
    
Renddata é os dados associados à estrutura **Renddata** que contém as informações de renderização para o anexo correspondente. A estrutura **RENDDATA** é definida no TNEF. Arquivo de cabeçalho H. 
  
 _Att_Attribute_Seq:_
  
>  _Att_Attribute Att_Attribute Att_Attribute_Seq_
    
 _Att_Attribute:_
  
> Atributo **LVL_ATTACHMENT** -atributo de ID-soma de verificação de dados 
    
O atributo-ID, o tamanho do atributo e o atributo-dados têm as mesmas médias para o item Msg_Attribute.
  

