---
title: Assinar digitalmente dados em formulários do InfoPath
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 7b396d9f-9a47-3170-367f-5d1f0144f927
description: Uma assinatura digital é uma marca eletrônica segura, baseada em criptografia de autenticação em uma macro ou um documento. Uma assinatura digital válida confirma que os dados do signatário e não tem sido alterados desde que foi assinado. Quando estiver conectados documentos ou determinados dados nos documentos, a assinatura é computada e adicionada ao documento. Dessa forma, as assinaturas sempre percorrida com os dados assinados.
ms.openlocfilehash: dc839d0751d2e7aeb6f9eaccc3a86ce95e5228e2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765586"
---
# <a name="digitally-signing-data-in-infopath-forms"></a>Assinar digitalmente dados em formulários do InfoPath

Uma assinatura digital é uma marca eletrônica segura, baseada em criptografia de autenticação em uma macro ou um documento. Uma assinatura digital válida confirma que os dados do signatário e não tem sido alterados desde que foi assinado. Quando estiver conectados documentos ou determinados dados nos documentos, a assinatura é computada e adicionada ao documento. Dessa forma, as assinaturas sempre percorrida com os dados assinados.
  
Para assinar dados, os usuários precisam solicitar um certificado de autoridade de certificação e usá-lo para criar assinaturas digitais. A autoridade de certificação irá gerenciar o ciclo de vida dos certificados e chaves (públicas ou privadas) necessária para criptografar dados e criar a assinatura.
  
Usuários subsequentes do documento precisarão verificar assinaturas existentes e conforme o resultado da verificação, podem adicionar suas próprias contribuição e assinar. Para resultados de verificação precisas, o verificador deve confiar na autoridade de certificação que emitiu o certificado que foi usada para assinar originalmente o documento.
  
Assinaturas digitais XML são projetadas para transações que envolvem dados e documentos XML. O poder do assinaturas XML permanece na capacidade de entrar somente dados específicos em um documento XML.
  
## <a name="types-of-digital-signatures-in-infopath-forms"></a>Tipos de assinaturas digitais nos formulários do InfoPath

Microsoft InfoPath implementa as assinaturas digitais para ajudar a proteger os dados nos formulários do InfoPath. Dois tipos de assinaturas digitais estão presentes no InfoPath:
  
- Assinaturas digitais que garantem a integridade dos dados e a autenticidade do modelo de formulário (arquivo. xsn)
    
- Assinaturas digitais que garantem a integridade, autenticidade e suporte para não-recusa relacionada a dados em formulários XML
    
Enquanto a primeira categoria de assinaturas concentrando-se o modelo de formulário (arquivo. xsn), a segunda categoria refere-se os dados reais inseridos pelo usuário nos arquivos de formulário do InfoPath (arquivos. xml), onde o designer de formulários pode permitir que os usuários criem assinaturas digitais para todo o formulário ou seções do formulário. Há algumas diferenças fundamentais entre um modelo de assinadas e um formulário assinado. Embora este documento terá algumas referências aos modelos assinadas (como uma maneira alternativa de criar um formulário que será executado como totalmente confiável), ele não fornece detalhes sobre esse tipo de assinatura. Para obter mais informações sobre como assinar os modelos de formulário, consulte [Implantando modelos de formulário InfoPath assinado](deploying-signed-infopath-form-templates.md) o foco deste tópico é usando formulários do InfoPath XML assinados. Assinaturas digitais criadas pelo InfoPath para assinar dados em formulários XML de acordo com as especificações de assinaturas digitais do W3C XML. 
  
## <a name="digital-signatures-features"></a>Recursos de assinaturas digitais

InfoPath oferece um recurso de assinaturas digitais estendidas, com os desenvolvedores de modelo poder criar formulários flexíveis que ativar as assinaturas digitais para o formulário inteiro ou para dados específicos no formulário. Enquanto assinar digitalmente o formulário inteiro sempre criará contadores assinaturas para o formulário como uma entidade, assinatura de partes de formulários do InfoPath permite maior flexibilidade para escolher o tipo de relacionamento entre assinaturas adicionadas para o mesmo conjunto de dados: pode haver assinaturas de colegas, assinaturas de contador ou somente uma assinatura permitido.
  
Com a assinatura, InfoPath também adicionará por padrão algumas informações não-recusa para identificar os dados de usuários vimos no modo de exibição atual, bem como o tempo e outras configurações de ambiente, conforme elas foram definidas quando a assinatura foi criada. As informações de não-recusa podem ser personalizadas, mas somente os dados de nós de não-recusa padrão serão exibidos na caixa de diálogo não repúdio.
  
Para adicionar uma assinatura, os usuários têm que selecionar o conjunto de dados que serão assinados. O conjunto de dados que podem ser assinados é definido pelo criador do modelo de formulário e usado para assinar os dados durante o preenchimento do formulário. Para cada assinatura, os usuários terão que execute o Assistente de uma assinatura digital para selecionar o conjunto de dados assinados, selecionando um certificado, adicionando comentários e aprovando e confirmar a assinatura ao formulário.
  
Quando um usuário pausa o mouse sobre um controle que contém os dados assinados, o InfoPath exibirá uma indicação visual que os dados são assinados e não podem ser alterados. Os designers de modelo de formulário podem optar por ter as assinaturas exibidas no modo de exibição com os dados assinados, para que os usuários podem se beneficiar do acesso fácil para as informações de não-recusa.
  
## <a name="programmatic-support-for-digital-signatures"></a>Suporte programático para assinaturas digitais

O modelo de objeto do InfoPath inclui suporte para assinaturas digitais, que permite aos desenvolvedores acesso programático aos conjuntos de dados assinados são definidas no formulário por meio da classe [SignedDataBlockCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlockCollection.aspx) , e as assinaturas atribuído a cada conjunto de conectado a dados por meio da classe [SignatureCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignatureCollection.aspx) e para o certificado que é usado para criar uma assinatura por meio da classe de [certificado](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Certificate.aspx) . Além disso, o manipulador de eventos de [entrada](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Sign.aspx) é personalizável em formulários totalmente confiáveis, que oferece suporte para processamento avançado de assinaturas digitais nos formulários do InfoPath. 
  
## <a name="interoperability"></a>Interoperabilidade

A infraestrutura para assinaturas digitais no InfoPath foi criada usando o suporte a assinaturas digitais em MSXML5, de forma que as assinaturas digitais do InfoPath têm interoperabilidade completa com MSXML5 de assinaturas digitais.
  
Os formulários do InfoPath assinados e assinaturas digitais, criadas pelo InfoPath também fornecerá total interoperabilidade com assinaturas digitais criadas usando o Microsoft .NET Framework (começando com a versão 1.1). Assinaturas criadas pelo InfoPath podem ser verificadas por aplicativos que usam classes de verificação de assinatura do .NET Framework. Assinaturas criadas para dados hospedados nos formulários do InfoPath por aplicativos criados usando classes do .NET Framework assinaturas digitais são verificadas com êxito pelo mecanismo de assinaturas digitais do InfoPath.
  
## <a name="see-also"></a>Confira também



[Trabalhar com Assinaturas Digitais](how-to-work-with-digital-signatures.md)

