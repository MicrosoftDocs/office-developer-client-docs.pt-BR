---
title: ImPlantando modelos de formulário do InfoPath assinados
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 8345a4bc-ad7b-d0b0-7615-f77ade35006d
description: Antes de ler este tópico, confira a Templatessection de formulários assinados em conceitos de segurança adicionais do InfoPath para compreender a segurança do modelo de formulário assinado. As informações e as discussões nos tópicos níveis de segurança, implantação de email e modelos de formulário remoto também são relevantes.
ms.openlocfilehash: 76cc6dfdbd2c01827182c348281a98ad7cd17b69
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303714"
---
# <a name="deploying-signed-infopath-form-templates"></a>ImPlantando modelos de formulário do InfoPath assinados

Antes de ler este tópico, consulte a seção "modelos de formulário assinados" nos [conceitos de segurança adicionais do InfoPath Forms](additional-infopath-form-security-concepts.md) para compreender a segurança do modelo de formulário assinado. As informações e as discussões nos tópicos [níveis de segurança, implantação de email e modelos de formulário remoto](security-levels-email-deployment-and-remote-form-templates.md) também são relevantes. 
  
## <a name="digitally-signing-a-form-template"></a>Assinar digitalmente um modelo de formulário

Se você assinar digitalmente um modelo de formulário, você pode definir o nível de segurança do modelo de formulário como confiança total, o que significa que o formulário pode acessar arquivos e configurações no computador do usuário ou em um domínio diferente. (Além disso, assinar digitalmente um modelo de formulário não impede que você use outros níveis de segurança, se preferir. Você define o nível de segurança de um modelo de formulário assinado para o domínio ou nível de segurança restrito.) Além disso, você pode implantar o modelo de formulário assinado para usuários que estejam usando um programa de email e, em seguida, atualizar automaticamente o modelo de formulário assinado enviando a versão atualizada para os usuários como um anexo para uma mensagem de email, siga estas etapas:
  
### <a name="to-digitally-sign-a-form-template"></a>Para assinar digitalmente um modelo de formulário

1. No designer do InfoPath, clique na guia **arquivo** e, em seguida, clique em **Opções de formulário** na guia **informações** . 
    
2. Na caixa de diálogo **Opções de Formulário**, clique na categoria **Segurança e Confiabilidade**. 
    
3. Em **assinatura de modelo de formulário**, marque a caixa de seleção **assinar este modelo de formulário** . 
    
4. Clique em **Selecionar certificado**.
    
5. Na caixa de diálogo **Selecionar certificado** , clique no certificado que você deseja usar para assinar digitalmente o formulário. 
    
> [!NOTE]
> O botão **criar certificado** na caixa de diálogo **Opções de formulário** pode ser usado para gerar um certificado de teste para assinar um modelo de formulário. O certificado de teste deve ser usado para assinar modelos de formulário somente para teste. Os certificados de teste não devem ser usados para assinar modelos de formulário que serão distribuídos publicamente. Como os certificados não são emitidos por uma autoridade de certificação cujo certificado raiz já é confiável no computador de um usuário, o certificado de teste não será validado corretamente no computador do usuário. Se você implantar um modelo de formulário assinado com um certificado de teste, os usuários do modelo de formulário provavelmente não conseguirão abri-lo. 
  
## <a name="establishing-a-trusted-root-certificate-and-publisher"></a>Estabelecendo um certificado raiz confiável e o Publisher

 O certificado raiz confiável do certificado usado para assinar o modelo de formulário deve estar no repositório de certificados raiz confiáveis no computador cliente. Caso contrário, o editor do modelo de formulário não poderá ser verificado, e os usuários do modelo de formulário não terão a opção de confiar no editor. Se o certificado raiz confiável estiver no repositório de certificados raiz confiáveis, mas o editor não estiver na lista de editores confiáveis, os usuários serão solicitados e terão a opção de confiar no fornecedor do modelo de formulário. 
  
> [!NOTE]
> Se um modelo de formulário assinado solicitar um acesso restrito ou de domínio, o InfoPath usará a assinatura para verificar se o modelo de formulário não foi adulterado depois de ser assinado. O InfoPath também usa a assinatura para determinar se o modelo de formulário pode ser atualizado automaticamente. 
  
## <a name="deploying-signed-form-templates-with-full-trust-access"></a>ImPlantando modelos de formulário assinados com acesso de confiança total

O principal cenário para implantar modelos de formulário assinados é habilitar a funcionalidade do tipo domínio, como a atualização automática, em formulários de confiança total. Um modelo de formulário assinado que solicita acesso de confiança total tem o mesmo acesso aos recursos do sistema como um *formulário totalmente confiável* . Para um discussão detalhada sobre como funcionam os formulários totalmente confiáveis e sobre como criá-los e implantá-los, consulte [Noções básicas sobre formulários totalmente confiáveis](understanding-fully-trusted-forms.md).
  
No enTanto, dependendo do ambiente de computação da sua organização, você pode preferir usar modelos de formulário assinados ou formulários totalmente confiáveis. Por exemplo, há benefícios em usar um modelo de formulário assinado que solicita acesso de confiança total em vez de um formulário registrado e totalmente confiável. Um modelo de formulário assinado que solicita acesso de confiança total tem os seguintes benefícios:
  
- Não precisa ser registrado, diferentemente de um modelo de formulário totalmente confiável e não assinado.
    
- Habilita a atualização automática silenciosa do modelo de formulário.
    
Como você não precisa registrar um modelo de formulário assinado que solicita acesso de confiança total, não é necessário usar um pacote de instalação ou um arquivo de script para implantá-lo. Esse benefício simplifica muito a implantação de um modelo de formulário de confiança total.
  
Ao atualizar o modelo de formulário assinado que solicita acesso de confiança total, você pode apenas enviar o modelo atualizado para o usuário ou atualizá-lo em um local compartilhado. Quando o usuário abrir o modelo atualizado, o usuário não será solicitado, e a versão atualizada substituirá silenciosamente a cópia mais antiga no computador do usuário. Se você atualizou o modelo em um local compartilhado, o usuário poderá usar a cópia atualizada sem ser solicitado.
  
Se você quiser atualizar um formulário totalmente confiável e não assinado, deverá reempacotar o formulário e registrá-lo novamente. Além disso, um modelo de formulário totalmente confiável instalado e existente funciona apenas para o caminho do computador local, mas não funciona para um caminho de rede, porque o processo de registro não dá suporte à alteração de um caminho de computador local para um caminho de rede. No enTanto, como um certificado é necessário para assinar um modelo de formulário, você pode preferir implantar modelos de formulário totalmente confiáveis e registrados, se não quiser comprar um certificado.
  
## <a name="deploying-signed-form-templates-with-domain-or-restricted-access"></a>ImPlantando modelos de formulário assinados com acesso restrito ou de domínio

Um modelo de formulário assinado que tem um nível de segurança restrito ou de domínio também tem a vantagem da funcionalidade de atualização automática. Por exemplo, você pode publicar um modelo de formulário assinado em uma biblioteca de documentos em um servidor que esteja executando o Microsoft SharePoint Foundation ou em um servidor que tenha um nível de segurança de domínio. Quando você atualizar o modelo de formulário no local compartilhado, os usuários receberão a cópia atualizada automaticamente.
  

