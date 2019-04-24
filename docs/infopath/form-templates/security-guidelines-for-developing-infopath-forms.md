---
title: Diretrizes de segurança para desenvolver formulários do InfoPath
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 4690028e-20ac-297b-4651-801f5159c747
description: Antes de ler este tópico, confira conceitos adicionais de segurança de formulário do InfoPath para obter uma compreensão geral do modelo de segurança do InfoPath.
ms.openlocfilehash: 5108d8b1967b72ac4805f892bcf3bbae3aecccbe
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32299920"
---
# <a name="security-guidelines-for-developing-infopath-forms"></a>Diretrizes de segurança para desenvolver formulários do InfoPath

Antes de ler este tópico, confira [conceitos adicionais de segurança de formulário do InfoPath](additional-infopath-form-security-concepts.md) para obter uma compreensão geral do modelo de segurança do InfoPath. 
  
## <a name="security-issues-for-users-of-infopath-forms"></a>Problemas de segurança para usuários de formulários do InfoPath

As principais preocupações de segurança para os usuários do Microsoft InfoPath são semelhantes àquelas para aplicativos Web executados no Internet Explorer. No entanto, você deve observar que o nível de segurança fornecido para um formulário depende apenas de onde o modelo de formulário está localizado e não de onde os usuários armazenam ou abrem os documentos XML resultantes criados por eles. Os usuários podem determinar o local do modelo de formulário no qual estão trabalhando, examinando a barra de status no InfoPath.
  
O InfoPath ajuda a proteger os usuários contra as seguintes ameaças potenciais causadas por modelos de formulário criados maliciosamente:
  
- A possibilidade de divulgação de informações confidenciais do computador local ou de fontes de dados remotas.
    
- O uso mal-intencionado de controles ActiveX.
    
- O uso mal-intencionado de propriedades e métodos do modelo de objeto do InfoPath.
    
## <a name="disclosure-of-sensitive-information"></a>Divulgação de informações confidenciais

O cenário mais comum para a divulgação de informações confidenciais pode ocorrer se um autor de formulário mal-intencionado cria um formulário que usa as credenciais de segurança do usuário atual para acessar uma fonte de dados em um domínio diferente daquele no qual o próprio formulário foi implantado. Por exemplo, um usuário mal-intencionado pode enviar um formulário por mensagem de email ou usando uma URL para um formulário em um compartilhamento privado ou servidor Web. O formulário pode conter um script que executa uma solicitação de acesso a dados usando as credenciais do usuário atual para recuperar dados de uma fonte de dados em outro domínio para o qual o usuário mal-intencionado não teria acesso, como um banco de dados de folha de pagamento ou outro confidencial Information. Essa classe de cenários de risco de segurança é chamada de acesso de dados entre domínios.
  
O modelo de segurança do Internet Explorer no qual o InfoPath é criado fornece uma configuração chamada **acessar fontes de dados entre domínios** que, por padrão, desabilita o acesso entre domínios para formulários do InfoPath que residem na **Internet** e são **restritos **zonas de segurança de sites. Essa configuração também solicita ao usuário para permitir ou impedir o acesso entre domínios para formulários do InfoPath que residem na zona de segurança **da intranet local** e permite o acesso entre domínios para formulários do InfoPath que residem nos **sites confiáveis** ou **local **Zonas de máquina. 
  
## <a name="malicious-use-of-activex-controls"></a>Uso mal-intencionado de controles ActiveX

O cenário principal para o uso mal-intencionado de controles ActiveX é quando um autor de formulário mal-intencionado grava código em um controle ActiveX que acessa o sistema de arquivos para recuperar arquivos pessoais e listas de senhas, excluir arquivos ou desabilitar o sistema do usuário. Um formulário do InfoPath pode executar código em controles ActiveX somente a partir da lógica de negócios ou de script em execução em um painel de tarefas. O InfoPath não permite que scripts nos modos de exibição do InfoPath executem controles ActiveX.
  
O modelo de segurança do Internet Explorer no qual o InfoPath é criado fornece uma configuração chamada **inicializar e script controles ActiveX marcados como não seguros**. Essa configuração, por padrão, desabilita a inicialização e o script de controles ActiveX marcados como não seguros para os formulários do InfoPath que residem nas zonas de segurança **intranet local**, **Internet**e **sites restritos** . Ele solicita ao usuário para permitir ou não o script de controles ActiveX marcados como não seguros para formulários do InfoPath que residem nas zonas de segurança de **sites confiáveis** ou de **máquina local** e permite o script de controles ActiveX marcados como não seguros para Formulários do InfoPath que são totalmente confiáveis. 
  
Além disso, você não pode inserir um controle ActiveX que está marcado como não seguro para inicializar e criar scripts no painel de tarefas controles enquanto estiver no modo de design, independentemente da zona de segurança em que você está ou do nível de confiança do formulário.
  
## <a name="malicious-use-of-infopath-object-model-code"></a>Uso mal-intencionado do código de modelo de objeto do InfoPath

Da mesma forma, os métodos e propriedades do InfoPath chamados do código podem apresentar diferentes níveis de risco. Por exemplo, o método [SaveAs(String)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.SaveAs.aspx) da classe [XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) pode ser usado para gravar dados em qualquer local do sistema de arquivos. Para ajudar a proteger contra o uso mal-intencionado desses membros do modelo de objeto, o modelo de objeto do InfoPath implementa três níveis de segurança que determinam como e onde um determinado membro de modelo de objeto pode ser usado. Para obter mais informações sobre esse recurso, consulte [sobre o modelo de segurança para modelos de formulário com código](about-the-security-model-for-form-templates-with-code.md).
  
## <a name="best-practices-for-developers-of-infopath-forms"></a>Práticas recomendadas para desenvolvedores de formulários do InfoPath

Os desenvolvedores que criam formulários do InfoPath devem saber como implementar as seguintes práticas recomendadas de segurança:
  
- Como reconhecer possíveis problemas de segurança no arquivo XML associado a um formulário.
    
- Como evitar a apresentação de mensagens de erro confusas ou irritantes para os usuários de formulários.
    
- Como assinar os arquivos CAB dos controles ActiveX.
    
- Como assinar modelos de formulário enviados como um anexo para uma mensagem de email.
    
## <a name="best-practices-for-xml-data-associated-with-a-form"></a>Práticas recomendadas para dados XML associados a um formulário

Observe que os formulários do InfoPath podem ser alimentados em dados XML de qualquer fonte, incluindo aqueles que o usuário não necessariamente confia ou controla. Por exemplo, o InfoPath pode obter dados XML de um link para uma página da Web ou de um anexo XML enviado ao usuário em uma mensagem de email. Para reduzir esses riscos, esteja ciente das seguintes práticas recomendadas:
  
- Não transmita dados não confiáveis que são lidos do XML para a função **Eval ()** do Microsoft JScript ou a propriedade **InnerHtml** do painel de tarefas. Ambas as chamadas podem ser usadas para executar um script mal-intencionado. Em um painel de tarefas, use a propriedade **InnerText** como uma alternativa. Observe que os modos de exibição do InfoPath não podem executar o script. 
    
- Os dados enviados para um banco de dados de um arquivo XML podem apresentar riscos de segurança para o banco de dados se ele não for validado antes do envio.
    
Os dados que não são validados antes de serem reenviados para uma fonte de dados podem danificar a integridade dos dados na fonte de dados, ou em casos mais extremos, apresentar o potencial para saturações de buffer. Também é possível causar injeção de script ou injeção de SQL, se você tentar usar dados não confiáveis diretamente no servidor.
  
## <a name="best-practices-to-avoid-presenting-confusing-error-messages"></a>Práticas recomendadas para evitar a apresentação de mensagens de erro confusas

 **Implantar formulários e suas fontes de dados no mesmo domínio**
  
O risco de segurança do acesso a dados entre domínios não é claramente compreendido pela maioria dos usuários. A implantação de formulários que avisam continuamente e avisam os usuários sobre a permissão de acesso de dados entre domínios tem o efeito de treinar muitos usuários para aprovar todas as solicitações de acesso entre domínios ou para adicionar o domínio de origem à sua lista de **sites confiáveis** , sem fazer os riscos de segurança seriamente. Para evitar essa situação, implante os formulários do InfoPath no mesmo servidor que qualquer fonte de dados que dependa. 
  
 **Evite usar controles ActiveX que não estejam marcados como seguros para scripts**
  
Os controles ActiveX podem expor propriedades e métodos que podem ser usados para comprometer o sistema de um usuário, como métodos para acessar o sistema de arquivos de um computador. Sempre que possível, você deve usar somente os controles ActiveX marcados como seguros para script. Estes são controles que foram testados para garantir que eles não danificarão o sistema de um usuário ou comprometem a segurança do usuário, independentemente de como os métodos e as propriedades do controle são manipulados pelo script de uma página da Web. Da mesma forma, ao criar controles ActiveX para uso com o InfoPath, inspecione o código e teste o controle ActiveX rigorosamente antes de marcá-lo como seguro para scripts.
  
O InfoPath usa um modelo de segurança baseado nas zonas de segurança do Internet Explorer. Portanto, um formulário do InfoPath usará as mesmas permissões que o Internet Explorer, que por padrão permite chamadas de script para controles ActiveX marcados como seguros para script, sem avisar os usuários.
  
## <a name="best-practices-for-managing-the-cab-files-of-activex-controls"></a>Práticas recomendadas para o gerenciamento de arquivos CAB de controles ActiveX

Os controles ActiveX podem ser hospedados em modelos de formulário projetados para o editor do InfoPath. Arquivos CAB para esses controles que ainda não estão presentes no computador do usuário devem ser incluídos no arquivo de modelo de formulário (. xsn). Os arquivos CAB incluídos nos modelos de formulário devem ser assinados digitalmente para que o arquivo CAB seja instalado. O InfoPath não instalará um arquivo CAB que não seja assinado, independentemente do nível de confiança ou da zona de segurança.
  
Para garantir que a assinatura digital no arquivo CAB possa ser verificada, o arquivo deve ser assinado com um certificado que tenha uma cadeia de confiança que leva a uma raiz de certificado já confiável. Caso contrário, a assinatura não poderá ser autenticada, a verificação da assinatura irá falhar e o arquivo CAB não será instalado.
  
## <a name="best-practices-for-form-templates-sent-as-an-attachment-to-an-email-message"></a>Práticas recomendadas para modelos de formulário enviados como um anexo para uma mensagem de email

O InfoPath oferece suporte à implantação de modelos de formulário como um anexo a uma mensagem de email e à movimentação de modelos de formulário de um local para outro. É uma boa prática de segurança assinar digitalmente um modelo de formulário que você designu e pretende implantar como um anexo para uma mensagem de email. Uma assinatura digital em um modelo de formulário implantado por mensagem de email não só garante a autenticidade do modelo. Ele também tem o benefício adicional de permitir que o modelo de formulário seja atualizado automaticamente.
  
O modelo de formulário deve ser assinado com um certificado que tenha uma cadeia de confiança que leva a uma raiz de certificado já confiável. Se ele não estiver assinado com esse certificado, a verificação da assinatura falhará, pois a assinatura não poderá ser autenticada.
  
> [!NOTE]
> Se um modelo de formulário assinado solicitar um domínio ou acesso restrito, o InfoPath não verificará ou verificará a assinatura, exceto determinará se o InfoPath pode atualizar automaticamente o modelo. 
  
Você pode encontrar mais informações sobre a implantação de email em [níveis de segurança, implantação de email e modelos de formulário remoto](security-levels-email-deployment-and-remote-form-templates.md).
  

