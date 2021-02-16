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
  
A série de ações a seguir descreve como os transporte usam métodos TNEF para processar mensagens de saída e de entrada.
  
 **Para enviar uma mensagem que inclui um fluxo TNEF**
  
1. Processe as propriedades de mensagem que são suportadas pelo sistema de mensagens.
    
2. Marque a mensagem de uma maneira específica de implementação para que o provedor de transporte de recebimento possa determinar que a mensagem requer processamento TNEF. Por exemplo, um provedor de transporte TNEF enviando para um sistema de mensagens SMTP pode adicionar um campo de header personalizado como "X-CONTAINS-TNEF" para indicar que a mensagem contém dados TNEF.
    
3. Obtenha um objeto TNEF e use-o para encapsular as propriedades de mensagem não suportadas pelo sistema de mensagens em um fluxo TNEF.
    
4. Codificar o fluxo TNEF usando o modelo de anexo do sistema de mensagens. Por exemplo, se o modelo de anexo subjacente for para codificar anexos e aendá-los ao texto da mensagem, o provedor de transporte deverá codificar o fluxo TNEF em outro anexo. O provedor de transporte também deve implementar um método para reconhecer qual anexo contém o fluxo TNEF codificado quando recebe uma mensagem. A maneira padrão de marcar esse anexo é dar a ele um nome de arquivo de anexo "WINMAIL. DAT". Se o provedor de transporte fizer isso, qualquer outro provedor de transporte habilitado para TNEF que seguir essa convenção poderá interoperar com ela.
    
5. Use [ITnef : métodos](itnefiunknown.md) de interface IUnknown para inserir marcas que descrevem as posições dos anexos de mensagem no texto da mensagem. 
    
6. Acesse o texto da mensagem marcado por [meio dos métodos IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) e envie-o para o sistema de mensagens. 
    
 **Para recuperar propriedades encapsuladas**
  
1. Escreva as propriedades suportadas pelo sistema de mensagens em uma nova mensagem, incluindo o texto da mensagem marcado que contém as propriedades encapsuladas.
    
2. Decodificar o fluxo TNEF do anexo apropriado.
    
3. Decodificar quaisquer outros anexos e gravar em novos anexos MAPI em uma mensagem.
    
4. Abra o fluxo TNEF para decodificação usando a [função OpenTnefStreamEx.](opentnefstreamex.md) 
    
5. Use o [método ITnef::ExtractProps](itnef-extractprops.md) para decodificar o fluxo TNEF e gravar as propriedades encapsuladas na nova mensagem. Quaisquer propriedades codificadas que sejam duplicatas de propriedades não codificadas substituirão as propriedades não codificadas quando as propriedades codificadas são decodificadas. 
    
6. Use o [método ITnef::OpenTaggedBody](itnef-opentaggedbody.md) para analisar o texto da mensagem para recuperar posições de anexo das marcas no texto da mensagem. 
    

