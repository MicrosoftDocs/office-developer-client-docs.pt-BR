---
title: Implantando modelos de formulário do InfoPath assinado
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 8345a4bc-ad7b-d0b0-7615-f77ade35006d
description: Antes de ler este tópico, consulte theSigned Templatessection de formulário em conceitos adicionais de segurança de formulário do InfoPath para a compreensão de segurança do modelo de formulário assinado. Discussões no tópico níveis de segurança, implantação de email e modelos de formulário remotos e informações também são relevantes.
ms.openlocfilehash: de64cb0efdbbdd11a301d89ced03e63454849adb
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765590"
---
# <a name="deploying-signed-infopath-form-templates"></a>Implantando modelos de formulário do InfoPath assinado

Antes de ler este tópico, consulte a seção "Modelos de formulário assinados" [Conceitos adicionais de segurança de formulário do InfoPath](additional-infopath-form-security-concepts.md) para a compreensão de segurança do modelo de formulário assinado. Discussões no tópico [níveis de segurança, implantação de email e modelos de formulário remotos](security-levels-email-deployment-and-remote-form-templates.md) e informações também são relevantes. 
  
## <a name="digitally-signing-a-form-template"></a>Assinar digitalmente um modelo de formulário

Se você assinar digitalmente um modelo de formulário, você pode definir o nível de segurança do modelo de formulário como confiança total, que significa que o formulário pode acessar arquivos e configurações no computador do usuário ou em um domínio diferente. (Além disso, assinar digitalmente um modelo de formulário não impede que você usar outros níveis de segurança, se você preferir. Defina o nível de segurança de um modelo de formulário assinado para o nível de segurança de domínio ou restrito.) Além disso, você pode implantar o modelo de formulário assinado aos usuários que estiver usando um programa de email e, em seguida, atualize o modelo de formulário assinado posteriormente automaticamente enviando a versão atualizada para os usuários como um anexo em uma mensagem de email, siga estas etapas:
  
### <a name="to-digitally-sign-a-form-template"></a>Para assinar digitalmente um modelo de formulário

1. No designer do InfoPath, clique na guia **arquivo** e clique em **Opções de formulário** , na guia **informações** . 
    
2. Na caixa de diálogo **Opções de formulário** , clique na categoria de **segurança e confiança** . 
    
3. Em **Assinatura do modelo de formulário**, marque a caixa de seleção de **entrada esse modelo de formulário** . 
    
4. Clique em **Selecionar certificado**.
    
5. Na caixa de diálogo **Selecionar certificado** , clique no certificado que você deseja usar para assinar digitalmente o formulário. 
    
> [!NOTE]
> Botão **Criar certificado** na caixa de diálogo **Opções de formulário** pode ser usado para gerar um certificado de teste para assinar um modelo de formulário. O certificado de teste deve ser usado para assinar os modelos de formulário somente para teste. Certificados de teste não devem ser usados para assinar os modelos de formulário que serão distribuídos publicamente. Porque os certificados não são emitidos por uma autoridade de certificação cujo certificado raiz já é confiável no computador do usuário, o certificado de teste não é validada corretamente no computador do usuário. Se você implantar um modelo de formulário assinado com um certificado de teste, os usuários de seu modelo de formulário mais provável poderão abri-lo. 
  
## <a name="establishing-a-trusted-root-certificate-and-publisher"></a>Estabelecendo um certificado raiz confiável e Publisher

 O certificado raiz confiável do certificado que é usado para assinar o modelo de formulário deve ser no repositório de certificados raiz confiável no computador cliente. Caso contrário, o fornecedor do modelo de formulário não puderem ser verificado e os usuários de seu modelo de formulário não terão a opção para confiar no Editor. Se o certificado raiz confiável é no repositório de certificados raiz confiáveis, mas o publisher não está na lista de editores confiáveis, os usuários são solicitados e a opção de confiar no Editor do modelo de formulário. 
  
> [!NOTE]
> Se um modelo de formulário assinado solicitar acesso domínio ou restrito, o InfoPath usará a assinatura para verificar se o modelo de formulário não foi adulterado após terem sido assinados. O InfoPath também usa a assinatura para determinar se o modelo de formulário pode ser atualizado automaticamente. 
  
## <a name="deploying-signed-form-templates-with-full-trust-access"></a>Implantando assinado modelos de formulário com acesso de confiança total

O cenário primário para implantação dos modelos de formulário assinado é habilitar a funcionalidade de domínio semelhantes, como a atualização automática, nos formulários de confiança total. Um modelo de formulário assinado solicitando acesso de confiança total tem o mesmo acesso aos recursos do sistema que um *totalmente confiáveis formulário* . Para uma discussão detalhada de como formulários totalmente confiáveis funcionam e como criar e implantá-las, consulte [Understanding totalmente confiáveis formulários](understanding-fully-trusted-forms.md).
  
No entanto, dependendo do ambiente de computação da sua organização, talvez você prefira usar modelos de formulário assinado ou formulários totalmente confiáveis. Por exemplo, existem benefícios de usar um modelo de formulário assinado que solicita acesso de confiança total, em vez de um formulário totalmente confiável registrado. Um modelo de formulário assinado solicitando acesso de confiança total tem os seguintes benefícios:
  
- Não precisa ser registrado, ao contrário de um modelo de formulário não assinados e totalmente confiável.
    
- Permite a atualização automática silenciosa do modelo de formulário.
    
Como você não precisa registrar um modelo de formulário assinado que solicita acesso de confiança total, você não precisa usar um arquivo de script ou de pacote do instalador para implantá-lo. Esse benefício simplifica bastante a implantação de um modelo de formulário de confiança total.
  
Quando você atualiza seu modelo de formulário assinado que solicita acesso de confiança total, basta enviar o modelo atualizado para o usuário ou atualizá-lo em um local compartilhado. Quando o usuário abre o modelo atualizado, o usuário não será solicitado e a versão atualizada silenciosamente substituirá a cópia mais antiga no computador do usuário. Se você atualizou o modelo em um local compartilhado, o usuário poderá usar a cópia atualizada sem que seja solicitado.
  
Se você deseja atualizar um formulário não assinado e totalmente confiável, você deve remonte seu formulário e registrá-lo novamente. Além disso, um modelo de formulário totalmente confiável existente, instalado funciona apenas para o caminho do computador local, mas não funciona para um caminho de rede, porque o processo de registro não dá suporte a alteração de um caminho de computador local para um caminho de rede. No entanto, porque é necessário um certificado para assinar um modelo de formulário, você talvez prefira implantar modelos de formulário totalmente confiável, registrados, se você não deseja comprar um certificado.
  
## <a name="deploying-signed-form-templates-with-domain-or-restricted-access"></a>Implantando modelos de formulário assinado com acesso restrito ou de domínio

Um modelo de formulário assinado que tem um nível de segurança de domínio ou restrito também tem a vantagem da funcionalidade de atualização automática. Por exemplo, você poderia publicar um modelo de formulário assinado para uma biblioteca de documentos em um servidor que está executando o Microsoft SharePoint Foundation ou em um servidor que tem um nível de segurança de domínio. Quando você atualiza seu modelo de formulário no local compartilhado, os usuários receberão a cópia atualizada automaticamente.
  

