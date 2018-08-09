---
title: Estrutura do fluxo de TNEF
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 8eda1251-3858-4832-ac43-d817b4a7ea59
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 0fcd1c79d1c0debfb18d270dc0e40de42842c6d9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770615"
---
# <a name="tnef-stream-structure"></a>Estrutura do fluxo de TNEF

  
  
**Aplica-se a**: Outlook 
  
Um fluxo TNEF começa com uma assinatura de 32 bits que identifica o fluxo como um fluxo TNEF. Após a assinatura é um inteiro não assinado de 16 bits que é usado como uma chave de anexos para seu local no texto da mensagem marcados de referência cruzada. O restante do fluxo é uma sequência de atributos TNEF. Atributos de mensagem aparecem primeiro no stream TNEF e siga os atributos de anexo. Atributos que pertencem a um determinado anexo são agrupados juntos, começando com o atributo **attAttachRenddata** . 
  
A maioria dos valores constantes usadas em fluxos TNEF forem definida no TNEF. Arquivo de cabeçalho H. Em especial, **TNEF_SIGNATURE**, **LVL_MESSAGE**, **LVL_ATTACHMENT**e todos os identificadores de atributo TNEF são definidos neste arquivo. Outras constantes têm os valores indicados por seu interpretação para um compilador de linguagem C. Geralmente, essas constantes são usadas para dar os tamanhos de item a seguir. Por exemplo, **sizeof(ULONG)** na definição de um item indica que um inteiro que representa o tamanho dos seguinte inteiro não assinado de longo deve ocorrer em que lugar no stream TNEF. 
  
Todos os números inteiros em um stream TNEF são armazenados em formato binário de pouca-endian, mas são mostrados em hexadecimal ao longo desta seção. Os valores de soma de verificação são números inteiros não assinados simplesmente de 16 bits são a soma, de 65536, dos bytes de dados que a soma de verificação se aplica ao módulo. Todos os comprimentos de atributo são inteiros longos não assinados, incluindo quaisquer caracteres encerramento de null.
  
A chave é um inteiro não assinado de 16 bits, diferente de zero, que significa o valor inicial das chaves de referência de anexo. As chaves de referência do anexo são atribuídas a cada anexo sequencialmente começando com o valor inicial que é passado para a função [OpenTnefStream](opentnefstream.md) pelo provedor de serviços que está usando o TNEF. O provedor de serviços deve gerar um valor inicial aleatório para a chave minimizar a chance de que as duas mensagens usam a mesma chave. 
  
A implementação de TNEF usa identificadores de atributo para mapear atributos às suas propriedades MAPI correspondentes. Um identificador de atributo é um inteiro não assinado de 32 bits formado por dois valores do word. A palavra de ordem alta indica o tipo de dados, como cadeia de caracteres ou binário, e a palavra de ordem baixa identifica o atributo específico. Os tipos de dados da palavra de ordem alta são:
  
|**Tipo de**|**Valor**|
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
   
Os valores de ordem baixa word para cada atributo são definidos no TNEF. Arquivo de cabeçalho H.
  

