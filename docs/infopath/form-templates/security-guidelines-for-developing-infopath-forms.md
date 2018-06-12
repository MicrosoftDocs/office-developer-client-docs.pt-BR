---
title: Diretrizes de segurança para o desenvolvimento de formulários do InfoPath
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 4690028e-20ac-297b-4651-801f5159c747
description: Antes de ler este tópico, consulte conceitos adicionais de segurança de formulário do InfoPath para ter uma compreensão geral do modelo de segurança do InfoPath.
ms.openlocfilehash: 3a72421882e655f34abd1eda30fe7e4fb42c45c0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765720"
---
# <a name="security-guidelines-for-developing-infopath-forms"></a>Diretrizes de segurança para o desenvolvimento de formulários do InfoPath

Antes de ler este tópico, consulte [Conceitos adicionais de segurança de formulário do InfoPath](additional-infopath-form-security-concepts.md) para ter uma compreensão geral do modelo de segurança do InfoPath. 
  
## <a name="security-issues-for-users-of-infopath-forms"></a>Problemas de segurança para usuários de formulários do InfoPath

As preocupações de segurança principal para usuários do Microsoft InfoPath são similares aos aplicativos Web em execução no Internet Explorer. No entanto, você deve observar que o nível de segurança fornecido para um formulário depende somente onde se encontra o modelo de formulário e não em onde os usuários armazenam ou abram documentos XML resultantes criarem. Os usuários podem determinar o local do modelo de formulário que eles estão trabalhando com examinando a barra de status no InfoPath.
  
O InfoPath ajuda a proteger os usuários contra as seguintes ameaças potenciais impostas por modelos de formulário de modo mal-intencionado criados:
  
- O potencial de divulgação de informações confidenciais do computador local ou fontes de dados remotos.
    
- O uso mal-intencionado de controles ActiveX.
    
- O uso mal-intencionado de propriedades e métodos do modelo de objeto do InfoPath.
    
## <a name="disclosure-of-sensitive-information"></a>Divulgação de informações confidenciais

O cenário mais comum para a divulgação de informações confidenciais pode ocorrer se um autor de formulário mal-intencionado cria um formulário que usa as credenciais de segurança do usuário atual para acessar uma fonte de dados em um domínio diferente em que o próprio formulário foi implantado. Por exemplo, um usuário malicioso pode enviar um formulário de mensagem de email ou usando uma URL para um formulário em um compartilhamento privado ou servidor Web. O formulário pode conter um script que realiza uma solicitação de acesso de dados, usando as credenciais do usuário atual para recuperar dados de uma fonte de dados em outro domínio que o usuário mal-intencionado caso contrário, não terá acesso, como um banco de dados de folha de pagamento ou outros confidenciais informações. Esta classe de cenários de riscos de segurança é conhecida como acesso a dados entre domínios.
  
O modelo de segurança do Internet Explorer InfoPath é construído fornece que uma configuração chamada **acessar fontes de dados entre domínios** que, por padrão, desabilita o acesso entre domínios para formulários do InfoPath que residem na **Internet** e **restrito sites** zonas de segurança. Essa configuração também solicita ao usuário para permitir ou não o acesso entre domínios para formulários do InfoPath que residem na zona de segurança **intranet Local** , e ela permite o acesso entre domínios para formulários do InfoPath que residem na **Local ou **sites confiáveis** Máquina** zonas. 
  
## <a name="malicious-use-of-activex-controls"></a>Uso mal-intencionado dos controles ActiveX

O cenário primário para o uso mal-intencionado de controles ActiveX é quando um autor de formulário mal-intencionado grava código contra um controle ActiveX que acessa o sistema de arquivos para recuperar arquivos pessoais e listas de senhas, excluir arquivos ou desabilitar o sistema do usuário. Um formulário do InfoPath pode executar código em relação a controles ActiveX, somente a partir de lógica de negócios ou script executado em um painel de tarefas. InfoPath não permitir scripts em modos de exibição do InfoPath executem controles ActiveX.
  
O modelo de segurança do Internet Explorer InfoPath é construído fornece que uma configuração chamada **inicializar e executar scripts de controles ActiveX não marcados como não seguros**. Essa configuração, por padrão, desabilita inicialização e script de controles ActiveX não marcados como seguros para formulários do InfoPath que residem em zonas de segurança da **intranet Local**, **Internet**e **sites restritos** . Solicita ao usuário para permitir ou não o script de controles ActiveX marcados como seguros para formulários do InfoPath que residem em **sites confiáveis** ou zonas de segurança da **Máquina Local** e permite que os scripts de controles ActiveX marcados como seguros para Formulários do InfoPath que são totalmente confiáveis. 
  
Além disso, você não pode inserir um controle que está marcado como seguros para inicialização e script no painel de tarefas controles ao mesmo tempo no modo de design, independentemente de qual zona de segurança que você está no controle ActiveX ou o nível de confiança do formulário.
  
## <a name="malicious-use-of-infopath-object-model-code"></a>Uso mal-intencionado de código do modelo de objeto do InfoPath

Da mesma forma, os métodos do InfoPath e as propriedades chamadas do código podem representar diferentes níveis de risco. Por exemplo, o método [SaveAs(String)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.SaveAs.aspx) da classe [XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) pode ser usado para gravar dados em qualquer lugar no sistema de arquivos. Para ajudar a proteger contra uso mal-intencionado desses membros do modelo de objeto, o modelo de objeto do InfoPath implementa três níveis de segurança que determinam como e onde um membro de modelo de objeto específico pode ser usado. Para obter mais informações sobre esse recurso, consulte [Sobre o modelo de segurança para modelos de formulário com código](about-the-security-model-for-form-templates-with-code.md).
  
## <a name="best-practices-for-developers-of-infopath-forms"></a>Práticas recomendadas para desenvolvedores de formulários do InfoPath

Desenvolvedores criando formulários do InfoPath devem saber como implementar as seguintes práticas recomendadas de segurança:
  
- Como reconhecer possíveis problemas de segurança no arquivo XML associado a um formulário.
    
- Como evitar a apresentação de mensagens de erro confusas e inconvenientes para os usuários do formulário.
    
- Como assinar os arquivos CAB dos controles ActiveX.
    
- Como assinar os modelos de formulário enviados como um anexo em uma mensagem de email.
    
## <a name="best-practices-for-xml-data-associated-with-a-form"></a>Práticas recomendadas para dados XML associados a um formulário

Observe que os formulários do InfoPath podem ser alimentados dados XML de qualquer origem, incluindo aquelas que o usuário não necessariamente confia ou controle. Por exemplo, o InfoPath pode obter dados XML a partir de um link para uma página da Web ou de um anexo XML enviado ao usuário na mensagem de email. Para atenuar esses riscos, esteja ciente das seguintes práticas recomendadas:
  
- Não passe dados não confiáveis que é lido a partir do XML para a função **Eval ()** Microsoft JScript ou a propriedade **innerHTML** do painel de tarefas. Ambas as chamadas podem ser usadas para executar o script mal-intencionado. Em um painel de tarefas, use a propriedade **innerText** como uma alternativa. Observe que modos de exibição do InfoPath não podem executar o script. 
    
- Dados enviados para um banco de dados de um arquivo XML podem representar os riscos de segurança no banco de dados se ele não é validado antes do envio.
    
Dados que não são validados antes de enviá-lo a uma fonte de dados pode danificar a integridade dos dados na fonte de dados ou em casos mais extremos, apresentam o potencial de estouros de buffer. Também é possível fazer a injeção de script ou injeção SQL, se você tentar usar dados não confiáveis diretamente no servidor.
  
## <a name="best-practices-to-avoid-presenting-confusing-error-messages"></a>Práticas recomendadas para evitar a apresentação de mensagens de erro confusas

 **Implantar formulários e suas fontes de dados no mesmo domínio**
  
O risco de segurança de acesso a dados entre domínios não é claramente compreendido pela maioria dos usuários. Implantando formulários que avisam e solicitam aos usuários sobre a permissão de acesso a dados entre domínios tem o efeito de treinar muitos usuários para aprovar todas as solicitações de acesso entre domínios ou para adicionar o domínio de origem à sua lista de **sites confiáveis** , sem fazer continuamente a segurança riscos seriamente. Para evitar essa situação, implante os formulários do InfoPath no mesmo servidor que as fontes de dados no qual eles dependem. 
  
 **Evite usando os controles ActiveX não marcados como seguros para script**
  
Os controles ActiveX podem potencialmente expor propriedades e métodos que podem ser usados para comprometer o sistema de um usuário, como métodos para acessar o sistema de arquivos de um computador. Sempre que possível, você deve usar somente os controles ActiveX que são marcados como seguros para script. Esses são controles que foram testados para garantir que eles não danificar o sistema de um usuário ou comprometer a segurança do usuário, independentemente de como os métodos e propriedades do controle são manipuladas pelo script de uma página Web. Da mesma forma, ao criar controles ActiveX para uso com o InfoPath, inspecionar o código e testar o controle ActiveX rigorosamente antes de marcar o seguros para script.
  
InfoPath usa um modelo de segurança que se baseia em zonas de segurança do Internet Explorer. Portanto, um formulário do InfoPath usará as mesmas permissões que o Internet Explorer, que, por padrão, permite que as chamadas de script para controles ActiveX marcados como seguros para script, sem avisar aos usuários.
  
## <a name="best-practices-for-managing-the-cab-files-of-activex-controls"></a>Práticas recomendadas de gerenciamento de arquivos CAB dos controles ActiveX

Os controles ActiveX podem ser hospedados em modelos de formulário projetados para o editor do InfoPath. Arquivos CAB para esses controles que ainda não estão presentes no computador do usuário devem ser incluídos no arquivo de modelo (. xsn) de formulário. Os arquivos CAB incluídos nos modelos de formulário devem ser assinados digitalmente na ordem para o arquivo CAB a ser instalado. InfoPath não instalará um arquivo CAB que não tiver entrado, independentemente da zona de segurança ou de nível de confiança.
  
Para garantir que a assinatura digital no arquivo CAB pode ser verificada, o arquivo deve ser assinado com um certificado que tenha uma cadeia de confiança que leva a uma raiz de certificado já seja confiável. Caso contrário, a assinatura não pode ser autenticada, a verificação da assinatura falhará e o arquivo CAB não será instalado.
  
## <a name="best-practices-for-form-templates-sent-as-an-attachment-to-an-email-message"></a>Práticas recomendadas para modelos de formulário enviados como um anexo em uma mensagem de Email

Modelos de um local para outro de formulário do InfoPath suporta a implantação de modelos de formulário como um anexo em uma mensagem de email e mover. É boa prática de segurança para assinar digitalmente um modelo de formulário que você cria e pretende implantar como um anexo em uma mensagem de email. Uma assinatura digital em um modelo de formulário implantado por mensagem de email não apenas garante a autenticidade do modelo. Ele também tem o benefício adicional de permitir que o modelo de formulário para serem atualizadas automaticamente.
  
O modelo de formulário deve ser assinado com um certificado que tenha uma cadeia de confiança que leva a uma raiz de certificado já seja confiável. Se ele não é assinado com esse certificado, verificação da assinatura falhará, porque a assinatura não poderão ser autenticada.
  
> [!NOTE]
> Se um modelo de formulário assinado solicitar acesso domínio ou restrito, o InfoPath não verifique ou verificar a assinatura exceto to determinar se o InfoPath pode atualizar automaticamente o modelo. 
  
Você pode encontrar mais informações sobre a implantação de email em [níveis de segurança, implantação de email e modelos de formulário remotos](security-levels-email-deployment-and-remote-form-templates.md).
  

