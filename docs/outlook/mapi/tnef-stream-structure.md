---
title: Estrutura de fluxo TNEF
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 8eda1251-3858-4832-ac43-d817b4a7ea59
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 7e77c043e4f152740af9bdb2b8fb5b7bedece1c0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430200"
---
# <a name="tnef-stream-structure"></a>Estrutura de fluxo TNEF

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Um fluxo TNEF começa com uma assinatura de 32 bits que identifica o fluxo como um fluxo TNEF. Após a assinatura há um inteiro não assinado de 16 bits que é usado como uma chave para fazer referência cruzada de anexos ao seu local no texto da mensagem marcada. O restante do fluxo é uma sequência de atributos TNEF. Os atributos de mensagem aparecem primeiro no fluxo TNEF e os atributos de anexo seguem. Os atributos que pertencem a um anexo específico são agrupados, começando com o **atributo attAttachRenddata.** 
  
A maioria dos valores constantes usados em fluxos TNEF é definida no TNEF. Arquivo de header H. Notavelmente, **TNEF_SIGNATURE**, **LVL_MESSAGE**, **LVL_ATTACHMENT** e todos os identificadores de atributo TNEF são definidos neste arquivo. Outras constantes têm os valores indicados por sua interpretação para um compilador da linguagem C. Normalmente, essas constantes são usadas para dar os tamanhos do item a seguir. Por exemplo, **sizeof(ULONG)** na definição de um item indica que um inteiro representando o tamanho do inteiro longo não assinado a seguir deve ocorrer nesse local no fluxo TNEF. 
  
Todos os inteiros em um fluxo TNEF são armazenados em forma binária little-endian, mas são mostrados em hexadecimal ao longo desta seção. Os valores de soma de verificação são simplesmente números inteiros não assinados de 16 bits que são a soma, modulo 65536, dos bytes de dados aos que a soma de verificação se aplica. Todos os comprimentos de atributos são inteiros longos não assinados, incluindo quaisquer caracteres nulos que terminam.
  
A chave é um inteiro não assinado de 16 bits que significa o valor inicial das chaves de referência do anexo. As chaves de referência de anexo são atribuídas a cada anexo sequencialmente começando com o valor inicial que é passado para a função [OpenTnefStream](opentnefstream.md) pelo provedor de serviços que está usando TNEF. O provedor de serviços deve gerar um valor inicial aleatório para a chave para minimizar a chance de duas mensagens usarem a mesma chave. 
  
A implementação do TNEF usa identificadores de atributos para mapear atributos para suas propriedades MAPI correspondentes. Um identificador de atributo é um inteiro não assinado de 32 bits, com dois valores de palavra. A palavra de ordem alta indica o tipo de dados, como cadeia de caracteres ou binário, e a palavra de ordem baixa identifica o atributo específico. Os tipos de dados na palavra de ordem alta são:
  
|**Tipo**|**Valor**|
|:-----|:-----|
|atpTriples  <br/> |0x0000  <br/> |
|atpString  <br/> |0x0001  <br/> |
|atpText  <br/> |0x0002  <br/> |
|atpDate  <br/> |0x0003  <br/> |
|atpShort  <br/> |0x0004  <br/> |
|atpLong  <br/> |0x0005  <br/> |
|atpByte  <br/> |0x0006  <br/> |
|atpWord  <br/> |0x0007  <br/> |
|atpDword  <br/> |0x0008  <br/> |
|atpMax  <br/> |0x0009  <br/> |
   
Os valores de palavras de ordem baixa para cada atributo são definidos no TNEF. Arquivo de header H.
  

