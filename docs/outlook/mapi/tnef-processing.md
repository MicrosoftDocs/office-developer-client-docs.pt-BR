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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25399564"
---
# <a name="tnef-processing"></a>Processamento TNEF

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
A série de ações a seguir descreve como transportes usam os métodos TNEF para processar as mensagens de entrada e saídas.
  
 **Para enviar uma mensagem que inclui um stream TNEF**
  
1. Processe as propriedades de mensagem que são suportadas pelo sistema de mensagens.
    
2. Marca a mensagem em uma implementação específica de maneira para que o provedor de transporte de recebimento possa determinar de que a mensagem requer processamento TNEF. Por exemplo, um provedor de transporte TNEF enviando para um sistema de mensagem SMTP pode adicionar um campo de cabeçalho personalizado como "X-contém-TNEF" para indicar que a mensagem contém dados TNEF.
    
3. Obter um objeto TNEF e usá-lo para encapsular as propriedades da mensagem não suportadas pelo sistema de mensagens em um fluxo TNEF.
    
4. Codifica fluxo TNEF, usando o modelo de anexo do sistema de mensagens. Por exemplo, se o modelo de anexo subjacente é uuencode anexos e acrescentá-las para o texto da mensagem, o provedor de transporte deve uuencode stream TNEF em outro anexo. O provedor de transporte também deve implementar um método para reconhecendo qual anexo contém o fluxo TNEF codificado quando ele recebe uma mensagem. A maneira padrão para marcar este anexo é dê a ela um nome de arquivo de anexo de "WINMAIL. DAT". Se o seu provedor de transporte faz isso, outros provedores de transporte habilitado TNEF que seguem Esta convenção poderão interoperar com ele.
    
5. Uso [ITnef: IUnknown](itnefiunknown.md) métodos para inserir marcações descrevendo as posições das anexos de mensagens no texto da mensagem de interface. 
    
6. Acessar o texto da mensagem marcados por meio dos métodos [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) e enviá-la para o sistema de mensagens. 
    
 **Para recuperar as propriedades encapsuladas**
  
1. Gravar as propriedades suportadas pelo sistema de mensagens em uma nova mensagem, incluindo o texto da mensagem sinalizada que contém as propriedades encapsuladas.
    
2. Decodificar o fluxo TNEF do anexo adequado.
    
3. Decodificar qualquer outro anexo e anotá-las para novos anexos de MAPI em uma mensagem.
    
4. Abra o fluxo TNEF para decodificação usando a função [OpenTnefStreamEx](opentnefstreamex.md) . 
    
5. Use o método [ITnef::ExtractProps](itnef-extractprops.md) para decodificar o fluxo TNEF e gravar as propriedades encapsuladas para a nova mensagem. Todas as propriedades codificadas duplicatas das propriedades nonencoded substituirá as propriedades nonencoded quando as propriedades codificadas são decodificadas. 
    
6. Use o método [ITnef::OpenTaggedBody](itnef-opentaggedbody.md) para analisar o texto da mensagem para recuperar as posições de anexo das marcas no texto da mensagem. 
    

