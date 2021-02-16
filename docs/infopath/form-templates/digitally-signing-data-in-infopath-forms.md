---
title: Assinatura digital de dados em formulários do InfoPath
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 7b396d9f-9a47-3170-367f-5d1f0144f927
description: Uma assinatura digital é um carimbo de autenticação eletrônico, baseado em criptografia e seguro em uma macro ou documento. Uma assinatura digital válida confirma que os dados se originaram do signante e não foram alterados desde que foram assinados. Quando documentos ou determinados dados nos documentos são assinados, a assinatura é calculada e adicionada ao documento. Dessa forma, as assinaturas sempre irão com os dados assinados.
ms.openlocfilehash: 6c1f5a1c14c15bc88839dc44d9a5a595d8b52893
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425096"
---
# <a name="digitally-signing-data-in-infopath-forms"></a>Assinatura digital de dados em formulários do InfoPath

Uma assinatura digital é um carimbo de autenticação eletrônico, baseado em criptografia e seguro em uma macro ou documento. Uma assinatura digital válida confirma que os dados se originaram do signante e não foram alterados desde que foram assinados. Quando documentos ou determinados dados nos documentos são assinados, a assinatura é calculada e adicionada ao documento. Dessa forma, as assinaturas sempre irão com os dados assinados.
  
Para assinar dados, os usuários precisam solicitar um certificado de uma autoridade de certificação e usá-lo para criar assinaturas digitais. A autoridade de certificação gerenciará o ciclo de vida dos certificados e chaves (públicas ou privadas) necessários para criptografar dados e criar a assinatura.
  
Os usuários subsequentes do documento terão que verificar as assinaturas existentes e, de acordo com o resultado da verificação, poderão adicionar sua própria contribuição e assinatura. Para resultados de verificação precisos, o verificador deve confiar na autoridade de certificação que emitiu o certificado que foi usado para assinar originalmente o documento.
  
As assinaturas digitais XML são projetadas para transações que envolvem dados e documentos XML. O poder das assinaturas XML permanece na capacidade de assinar somente dados específicos em um documento XML.
  
## <a name="types-of-digital-signatures-in-infopath-forms"></a>Tipos de assinaturas digitais em formulários do InfoPath

O Microsoft InfoPath implementa assinaturas digitais para ajudar a proteger dados em formulários do InfoPath. Dois tipos de assinaturas digitais são destaques no InfoPath:
  
- Assinaturas digitais que garantem a integridade e a autenticidade dos dados do modelo de formulário (arquivo .xsn)
    
- Assinaturas digitais que garantem a integridade, autenticidade e suporte para não repúdio relacionado a dados em formulários XML
    
Enquanto a primeira categoria de assinaturas está direcionando o modelo de formulário (arquivo .xsn), a segunda categoria direciona os dados reais inseridos pelo usuário em arquivos de formulário do InfoPath (arquivos .xml), onde o designer de formulário pode permitir que os usuários criem assinaturas digitais para todo o formulário ou para seções do formulário. Há diferenças fundamentais entre um modelo assinado e um formulário assinado. Embora este documento tenha algumas referências a modelos assinados (como uma maneira alternativa de criar um formulário que será executado como totalmente confiável), ele não fornece detalhes sobre esse tipo de assinatura. Para obter mais informações sobre como assinar modelos de formulário, consulte Implantando modelos de formulário assinados do [InfoPath.](deploying-signed-infopath-form-templates.md) O foco neste tópico é o uso de formulários XML assinados do InfoPath. As assinaturas digitais criadas pelo InfoPath para assinar dados em formulários XML estão em conformidade com as especificações de Assinaturas Digitais XML do W3C. 
  
## <a name="digital-signatures-features"></a>Recursos de Assinaturas Digitais

O InfoPath oferece um recurso estendido de assinaturas digitais, com os desenvolvedores de modelos capazes de criar formulários flexíveis que permitem assinaturas digitais para todo o formulário ou para dados específicos no formulário. Enquanto assinar digitalmente o formulário inteiro sempre criará contra-assinaturas para o formulário como uma entidade, assinar partes de formulários do InfoPath permite mais flexibilidade na escolha do tipo de relação entre assinaturas adicionadas ao mesmo conjunto de dados: pode haver co-assinaturas, contra-assinaturas ou apenas uma assinatura permitida.
  
Com a assinatura, o InfoPath também adicionará, por padrão, algumas informações de não repúdio para identificar os dados que os usuários visualizaram no modo de exibição atual, bem como a hora e outras configurações de ambiente definidas quando a assinatura foi criada. As informações de não repúdio podem ser personalizadas, mas somente os dados em nós de não repúdio padrão serão exibidos na caixa de diálogo de não repúdio.
  
Para adicionar uma assinatura, os usuários devem selecionar o conjunto de dados que será assinado. O conjunto de dados que pode ser assinado é definido pelo designer de modelo de formulário e usado para assinar os dados ao preencher o formulário. Para cada assinatura, os usuários terão que seguir um assistente de assinatura digital para selecionar o conjunto de dados signatáveis, selecionar um certificado, adicionar comentários e aprovar e assinar a assinatura para o formulário.
  
Quando um usuário passar o mouse sobre um controle que contém dados assinados, o InfoPath exibirá uma indicação visual de que os dados estão assinados e não podem ser alterados. Os designers de modelos de formulário podem optar por exibir as assinaturas na exibição com os dados assinados para que os usuários possam tirar proveito do acesso fácil às informações de não repúdio.
  
## <a name="programmatic-support-for-digital-signatures"></a>Suporte programático para assinaturas digitais

O modelo de objeto do InfoPath inclui suporte para assinaturas digitais, que permite aos desenvolvedores acesso programático aos conjuntos de dados signatáveis são definidos no formulário por meio da classe [SignedDataBlockCollection,](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlockCollection.aspx) para as assinaturas atribuídas a cada conjunto de dados assinados por meio da classe [SignatureCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignatureCollection.aspx) e para o certificado que é usado para criar uma assinatura por meio da classe [Certificate.](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Certificate.aspx) Além disso, o [manipulador de](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Sign.aspx) eventos Sign é personalizável em formulários totalmente confiáveis, oferecendo suporte para processamento avançado de assinaturas digitais em formulários do InfoPath. 
  
## <a name="interoperability"></a>Interoperabilidade

A infraestrutura para assinaturas digitais no InfoPath foi projetada usando o suporte a assinaturas digitais no MSXML5 para que as assinaturas digitais do InfoPath tenham total interoperabilidade com assinaturas digitais MSXML5.
  
Formulários assinados do InfoPath e assinaturas digitais criadas pelo InfoPath também fornecerão interoperabilidade completa com assinaturas digitais criadas usando o Microsoft .NET Framework (a partir da versão 1.1). Assinaturas criadas pelo InfoPath podem ser verificadas por aplicativos que usam classes de verificação de assinatura do .NET Framework. As assinaturas criadas para dados hospedados em formulários do InfoPath por aplicativos projetados usando classes de assinaturas digitais do .NET Framework são verificadas com êxito pelo mecanismo de assinaturas digitais do InfoPath.
  
## <a name="see-also"></a>Confira também



[Trabalhar com assinaturas digitais](how-to-work-with-digital-signatures.md)

