---
title: Processamento TNEF
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4d324fb3-d917-4502-b3a4-179c479deb79
description: '�ltima altera��o: quinta-feira, 5 de julho de 2012'
ms.openlocfilehash: 066ad3dfb64161e326b92fef7774d5b3b9461d8a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339596"
---
# <a name="tnef-processing"></a>Processamento TNEF

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
A série de ações a seguir descrevem como os transportes usam métodos TNEF para processar mensagens de saída e de entrada.
  
 **Para enviar uma mensagem que inclui um fluxo TNEF**
  
1. Processe as propriedades da mensagem que são suportadas pelo sistema de mensagens.
    
2. Marcar a mensagem em uma forma específica de implementação para que o provedor de transporte de recebimento possa determinar que a mensagem requer processamento TNEF. Por exemplo, um provedor de transporte TNEF enviando para um sistema de mensagens SMTP pode adicionar um campo de cabeçalho personalizado como "X-CONTAINS-TNEF" para indicar que a mensagem contém dados TNEF.
    
3. Obtenha um objeto TNEF e use-o para encapsular as propriedades de mensagem não suportadas pelo sistema de mensagens em um fluxo TNEF.
    
4. Codifique o fluxo TNEF usando o modelo de anexo do sistema de mensagens. Por exemplo, se o modelo de anexo subjacente for uuencode anexos e acrescentá-los ao texto da mensagem, o provedor de transporte deverá uuencode o fluxo TNEF para outro anexo. O provedor de transporte também deve implementar um método para reconhecer qual anexo contém o fluxo TNEF codificado quando recebe uma mensagem. O modo padrão de marcar esse anexo é dar a ele um nome de arquivo de anexo de "WINMAIL. DAT ". Se o seu provedor de transporte fizer isso, todos os outros provedores de transporte habilitados para TNEF que seguirem essa Convenção poderão interoperar com ele.
    
5. Use os métodos de interface [ITnef: IUnknown](itnefiunknown.md) para inserir marcas descrevendo as posições dos anexos de mensagens no texto da mensagem. 
    
6. Acessar o texto da mensagem marcada por meio de métodos [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) e enviá-lo ao sistema de mensagens. 
    
 **Para recuperar propriedades encapsuladas**
  
1. Escreva as propriedades aceitas pelo sistema de mensagens em uma nova mensagem, incluindo o texto da mensagem marcada que contém as propriedades encapsuladas.
    
2. DeCodifique o fluxo TNEF do anexo adequado.
    
3. DeCodifique quaisquer outros anexos e grave-os em novos anexos MAPI em uma mensagem.
    
4. Abra o fluxo TNEF para decodificação usando a função [OpenTnefStreamEx](opentnefstreamex.md) . 
    
5. Use o método [ITnef:: ExtractProps](itnef-extractprops.md) para decodificar o fluxo TNEF e gravar as propriedades encapsuladas na nova mensagem. Quaisquer propriedades codificadas que sejam duplicatas de propriedades não codificadas substituirão as propriedades não codificadas quando as propriedades codificadas forem decodificadas. 
    
6. Use o método [ITnef:: OpenTaggedBody](itnef-opentaggedbody.md) para analisar o texto da mensagem para recuperar posições de anexo das marcas no texto da mensagem. 
    

