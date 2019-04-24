---
title: Assinar digitalmente dados em formulários do InfoPath
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 7b396d9f-9a47-3170-367f-5d1f0144f927
description: Uma assinatura digital é uma marca de autenticação eletrônica, baseada em criptografia e segura em uma macro ou em um documento. Uma assinatura digital válida confirma que os dados originados do signatário não foram alterados desde que foi assinado. Quando documentos ou determinados dados nos documentos são assinados, a assinatura é calculada e adicionada ao documento. Dessa forma, as assinaturas sempre irão viajar com os dados assinados.
ms.openlocfilehash: 6c1f5a1c14c15bc88839dc44d9a5a595d8b52893
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32300242"
---
# <a name="digitally-signing-data-in-infopath-forms"></a>Assinar digitalmente dados em formulários do InfoPath

Uma assinatura digital é uma marca de autenticação eletrônica, baseada em criptografia e segura em uma macro ou em um documento. Uma assinatura digital válida confirma que os dados originados do signatário não foram alterados desde que foi assinado. Quando documentos ou determinados dados nos documentos são assinados, a assinatura é calculada e adicionada ao documento. Dessa forma, as assinaturas sempre irão viajar com os dados assinados.
  
Para assinar dados, os usuários precisam solicitar um certificado de uma autoridade de certificação e usá-lo para criar assinaturas digitais. A autoridade de certificação gerenciará o ciclo de vida dos certificados e das chaves (pública ou privada) necessárias para criptografar dados e criar a assinatura.
  
Os usuários subsequentes do documento terão que verificar as assinaturas existentes e, de acordo com o resultado da verificação, podem adicionar sua própria contribuição e assinatura. Para obter resultados de verificação precisos, o verificador deve confiar na autoridade de certificação que emitiu o certificado usado para assinar o documento originalmente.
  
As assinaturas digitais XML foram projetadas para transações que envolvem documentos e dados XML. O poder das assinaturas XML fica na capacidade de assinar apenas dados específicos em um documento XML.
  
## <a name="types-of-digital-signatures-in-infopath-forms"></a>Tipos de assinaturas digitais em formulários do InfoPath

O Microsoft InfoPath implementa assinaturas digitais para ajudar a proteger dados nos formulários do InfoPath. Dois tipos de assinaturas digitais estão presentes no InfoPath:
  
- Assinaturas digitais que garantem a integridade e a autenticidade dos dados do modelo de formulário (arquivo. xsn)
    
- Assinaturas digitais que garantem a integridade, a autenticidade e o suporte para não repudiação relacionada a dados em formulários XML
    
Enquanto a primeira categoria de assinaturas está direcionando o modelo de formulário (arquivo. xsn), a segunda categoria direciona os dados reais inseridos pelo usuário nos arquivos de formulário do InfoPath (arquivos. xml), onde o designer de formulários pode permitir que os usuários criem assinaturas digitais para o todo ou para seções do formulário. Há diferenças fundamentais entre um modelo assinado e um formulário assinado. Embora este documento tenha algumas referências a modelos assinados (como uma maneira alternativa de criar um formulário que será executado como totalmente confiável), ele não fornece detalhes sobre esse tipo de assinatura. Para obter mais informações sobre como assinar modelos de formulário, consulte imPlantando [modelos de formulário assinados do InfoPath](deploying-signed-infopath-form-templates.md) o foco neste tópico é usar formulários assinados do InfoPath XML. Assinaturas digitais criadas pelo InfoPath para assinar dados em formulários XML estão de acordo com as especificações de assinaturas digitais do W3C XML. 
  
## <a name="digital-signatures-features"></a>Recursos de assinaturas digitais

O InfoPath oferece um recurso de assinaturas digitais estendidas, com os desenvolvedores de modelos sendo capazes de criar formulários flexíveis que permitem assinaturas digitais para o formulário inteiro ou para dados específicos no formulário. Enquanto a assinatura digital de todo o formulário sempre criará assinaturas de contador para o formulário como uma entidade, assinar partes de formulários do InfoPath permite mais flexibilidade na escolha do tipo de relação entre as assinaturas adicionadas ao mesmo conjunto de dados: pode haver co-assinaturas, assinaturas de contador ou apenas uma assinatura permitida.
  
Com a assinatura, o InfoPath também será adicionado por padrão algumas informações de não repúdio para identificar os dados que os usuários viram no modo de exibição atual, bem como o horário e outras configurações de ambiente, conforme foram definidos quando a assinatura foi criada. As informações de não repúdio podem ser personalizadas, mas somente os dados em nós de não recusa padrão serão exibidos na caixa de diálogo não Repudiation.
  
Para adicionar uma assinatura, os usuários precisam selecionar o conjunto de dados que serão assinados. O conjunto de dados que pode ser assinado é definido pelo designer de modelo de formulário e usado para assinar os dados durante o preenchimento do formulário. Para cada assinatura, os usuários terão que seguir um assistente de assinatura digital para selecionar o conjunto de dados assináveis, selecionando um certificado, adicionando comentários e aprovando e confirmando a assinatura para o formulário.
  
Quando um usuário posiciona o mouse sobre um controle que contém dados assinados, o InfoPath exibe uma indicação visual de que os dados estão assinados e não podem ser alterados. Os designers de modelo de formulário podem optar por ter as assinaturas exibidas no modo de exibição com os dados assinados para que os usuários possam aproveitar o acesso fácil às informações de não repúdio.
  
## <a name="programmatic-support-for-digital-signatures"></a>Suporte de programação para assinaturas digitais

O modelo de objeto do InfoPath inclui suporte para assinaturas digitais, que permite aos desenvolvedores o acesso programático aos conjuntos de dados assináveis são definidos no formulário por meio da classe [SignedDataBlockCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlockCollection.aspx) , às assinaturas atribuídas a cada conjunto de dados assinados por [](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignatureCollection.aspx) meio da classe signaturecollection e ao certificado usado para criar uma assinatura por meio da classe de [certificado](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Certificate.aspx) . Além disso, o manipulador de eventos [assinar](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Sign.aspx) é personalizável em formulários totalmente confiáveis, oferecendo suporte para processamento avançado de assinaturas digitais em formulários do InfoPath. 
  
## <a name="interoperability"></a>Interoperabilidade

A infraestrutura para assinaturas digitais no InfoPath foi criada usando o suporte a assinaturas digitais no MSXML5 para que as assinaturas digitais do InfoPath tenham uma interoperabilidade total com assinaturas digitais do MSXML5.
  
Formulários assinados do InfoPath e assinaturas digitais criadas pelo InfoPath também oferecem interoperabilidade total com assinaturas digitais criadas usando o Microsoft .NET Framework (começando com a versão 1,1). As assinaturas criadas pelo InfoPath podem ser verificadas por aplicativos que usam classes de verificação de assinatura do .NET Framework. As assinaturas criadas para dados hospedados em formulários do InfoPath por aplicativos criados usando as classes de assinaturas digitais do .NET Framework são verificadas com êxito pelo mecanismo de assinaturas digitais do InfoPath.
  
## <a name="see-also"></a>Confira também



[Trabalhar com assinaturas digitais](how-to-work-with-digital-signatures.md)

