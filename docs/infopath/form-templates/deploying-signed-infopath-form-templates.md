---
title: Implantando modelos de formulário assinados do InfoPath
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 8345a4bc-ad7b-d0b0-7615-f77ade35006d
description: Antes de ler este tópico, consulte oSigned Form Templatessection em Additional InfoPath Form Security Concepts para entender a segurança do modelo de formulário assinado. Informações e discussões no tópico Níveis de Segurança, Implantação de Email e Modelos de Formulário Remoto também são relevantes.
ms.openlocfilehash: 76cc6dfdbd2c01827182c348281a98ad7cd17b69
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426797"
---
# <a name="deploying-signed-infopath-form-templates"></a>Implantando modelos de formulário assinados do InfoPath

Antes de ler este tópico, consulte a seção "Modelos de Formulário Assinados" em Conceitos adicionais de segurança de formulário do [InfoPath](additional-infopath-form-security-concepts.md) para entender a segurança do modelo de formulário assinado. Informações e discussões no tópico Níveis [de Segurança, Implantação](security-levels-email-deployment-and-remote-form-templates.md) de Email e Modelos de Formulário Remoto também são relevantes. 
  
## <a name="digitally-signing-a-form-template"></a>Assinando digitalmente um modelo de formulário

Se você assinar digitalmente um modelo de formulário, poderá definir o nível de segurança do modelo de formulário como Confiança Total, o que significa que o formulário pode acessar arquivos e configurações no computador do usuário ou em um domínio diferente. (Além disso, assinar digitalmente um modelo de formulário não impede que você use outros níveis de segurança, se preferir. Você pode definir o nível de segurança de um modelo de formulário assinado para o nível de segurança Domínio ou Restrito.) Além disso, você pode implantar o modelo de formulário assinado para usuários que estão usando um programa de email e, posteriormente, atualizar automaticamente o modelo de formulário assinado enviando a versão atualizada aos usuários como um anexo para uma mensagem de email, siga estas etapas:
  
### <a name="to-digitally-sign-a-form-template"></a>Para assinar digitalmente um modelo de formulário

1. No designer do InfoPath, clique na guia **Arquivo** e, em seguida, clique em **Opções de** Formulário na **guia** Informações. 
    
2. Na caixa de diálogo **Opções de Formulário**, clique na categoria **Segurança e Confiabilidade**. 
    
3. Em **Assinatura de Modelo de Formulário**, marque a caixa de seleção Assinar este **modelo** de formulário. 
    
4. Clique **em Selecionar Certificado.**
    
5. Na caixa **de diálogo Selecionar** Certificado, clique no certificado que deseja usar para assinar digitalmente o formulário. 
    
> [!NOTE]
> O **botão Criar Certificado** na caixa de diálogo **Opções** de Formulário pode ser usado para gerar um certificado de teste para assinar um modelo de formulário. O certificado de teste deve ser usado para assinar modelos de formulário somente para teste. Os certificados de teste não devem ser usados para assinar modelos de formulário que serão distribuídos publicamente. Como os certificados não são emitidos por uma Autoridade de Certificação cujo certificado raiz já é confiável no computador de um usuário, o certificado de teste não será validado corretamente no computador do usuário. Se você implantar um modelo de formulário assinado com um certificado de teste, os usuários do modelo de formulário provavelmente não poderão abri-lo. 
  
## <a name="establishing-a-trusted-root-certificate-and-publisher"></a>Estabelecendo um certificado raiz confiável e um fornecedor

 O certificado raiz confiável do certificado usado para assinar o modelo de formulário deve estar no armazenamento de certificado raiz confiável no computador cliente. Caso não seja, o editor do modelo de formulário não poderá ser verificado, e os usuários do modelo de formulário não terão a opção de confiar no editor. Se o certificado raiz confiável estiver no armazenamento de certificado raiz confiável, mas o editor não estiver na lista de editores confiáveis, os usuários serão solicitados e receberão a opção de confiar no editor do modelo de formulário. 
  
> [!NOTE]
> Se um modelo de formulário assinado solicitar acesso restrito ou domínio, o InfoPath usará a assinatura para verificar se o modelo de formulário não foi adulterado depois de assinado. O InfoPath também usa a assinatura para determinar se o modelo de formulário pode ser atualizado automaticamente. 
  
## <a name="deploying-signed-form-templates-with-full-trust-access"></a>Implantando modelos de formulário assinados com acesso de confiança total

O cenário principal para implantar modelos de formulário assinados é habilitar a funcionalidade do tipo domínio, como a atualização automática, em formulários de confiança total. Um modelo de formulário assinado solicitando acesso de confiança total tem o mesmo acesso aos recursos do sistema como *um formulário totalmente confiável.* Para um discussão detalhada sobre como funcionam os formulários totalmente confiáveis e sobre como criá-los e implantá-los, consulte [Noções básicas sobre formulários totalmente confiáveis](understanding-fully-trusted-forms.md).
  
No entanto, dependendo do ambiente de computação da sua organização, você pode preferir usar modelos de formulário assinados ou formulários totalmente confiáveis. Por exemplo, há benefícios em usar um modelo de formulário assinado que solicita acesso de confiança total em vez de um formulário registrado e totalmente confiável. Um modelo de formulário assinado que solicita acesso de confiança total tem os seguintes benefícios:
  
- Não precisa ser registrado, ao contrário de um modelo de formulário totalmente confiável não assinado.
    
- Habilita a atualização automática silenciosa do modelo de formulário.
    
Como não é preciso registrar um modelo de formulário assinado que solicita acesso de confiança total, você não precisa usar um pacote do instalador ou um arquivo de script para implantá-lo. Esse benefício simplifica bastante a implantação de um modelo de formulário de confiança total.
  
Ao atualizar seu modelo de formulário assinado que solicita acesso de confiança total, você pode apenas enviar o modelo atualizado para o usuário ou atualizá-lo em um local compartilhado. Quando o usuário abre o modelo atualizado, ele não será solicitado e a versão atualizada substituirá silenciosamente a cópia mais antiga no computador do usuário. Se você atualizou o modelo em um local compartilhado, o usuário poderá usar a cópia atualizada sem ser solicitado.
  
Se você deseja atualizar um formulário não assinado e totalmente confiável, você deve reempacorá-lo e registrá-lo. Além disso, um modelo de formulário totalmente confiável instalado e existente funciona apenas para o caminho do computador local, mas não funciona para um caminho de rede, porque o processo de registro não suporta a alteração de um caminho de computador local para um caminho de rede. No entanto, como um certificado é necessário para assinar um modelo de formulário, você pode preferir implantar modelos de formulário totalmente confiáveis e registrados, se não quiser comprar um certificado.
  
## <a name="deploying-signed-form-templates-with-domain-or-restricted-access"></a>Implantando modelos de formulário assinados com domínio ou acesso restrito

Um modelo de formulário assinado que tenha um nível de segurança Domínio ou Restrito também tem a vantagem da funcionalidade de atualização automática. Por exemplo, você pode publicar um modelo de formulário assinado em uma biblioteca de documentos em um servidor que esteja executando o Microsoft SharePoint Foundation ou em um servidor que tenha um nível de segurança de Domínio. Quando você atualiza seu modelo de formulário no local compartilhado, os usuários receberão a cópia atualizada automaticamente.
  

