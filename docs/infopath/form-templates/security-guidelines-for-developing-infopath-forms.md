---
title: Diretrizes de segurança para o desenvolvimento de formulários do InfoPath
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 4690028e-20ac-297b-4651-801f5159c747
description: Antes de ler este tópico, consulte Conceitos adicionais de segurança de formulário do InfoPath para ter uma compreensão geral do modelo de segurança do InfoPath.
ms.openlocfilehash: 5108d8b1967b72ac4805f892bcf3bbae3aecccbe
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437809"
---
# <a name="security-guidelines-for-developing-infopath-forms"></a>Diretrizes de segurança para o desenvolvimento de formulários do InfoPath

Antes de ler este tópico, consulte [Conceitos adicionais de](additional-infopath-form-security-concepts.md) segurança de formulário do InfoPath para ter uma compreensão geral do modelo de segurança do InfoPath. 
  
## <a name="security-issues-for-users-of-infopath-forms"></a>Problemas de segurança para usuários de formulários do InfoPath

As principais preocupações de segurança dos usuários do Microsoft InfoPath são semelhantes às dos aplicativos Web em execução no Internet Explorer. No entanto, você deve observar que o nível de segurança fornecido a um formulário depende apenas de onde o modelo de formulário está localizado e não de onde os usuários armazenam ou abrem os documentos XML resultantes que eles criam. Os usuários podem determinar o local do modelo de formulário com o qual estão trabalhando observando a barra de status no InfoPath.
  
O InfoPath ajuda a proteger os usuários contra as seguintes ameaças possíveis, colocadas por modelos de formulário mal-intencionados:
  
- O potencial de divulgação de informações confidenciais do computador local ou de fontes de dados remotas.
    
- O uso mal-intencionado de controles ActiveX.
    
- O uso mal-intencionado de propriedades e métodos do modelo de objeto do InfoPath.
    
## <a name="disclosure-of-sensitive-information"></a>Divulgação de informações confidenciais

O cenário mais comum para a divulgação de informações confidenciais poderá ocorrer se um autor de formulário mal-intencionado criar um formulário que use as credenciais de segurança do usuário atual para acessar uma fonte de dados em um domínio diferente aquele em que o próprio formulário foi implantado. Por exemplo, um usuário mal-intencionado pode enviar um formulário por email ou usando uma URL para um formulário em um compartilhamento particular ou servidor Web. O formulário pode conter um script que executa uma solicitação de acesso a dados usando as credenciais do usuário atual para recuperar dados de uma fonte de dados em outro domínio ao que o usuário mal-intencionado não teria acesso, como um banco de dados de folha de pagamento ou outras informações confidenciais. Essa classe de cenários de risco de segurança é conhecida como acesso a dados entre domínios.
  
O modelo de segurança do Internet Explorer no qual o InfoPath é criado fornece uma configuração chamada fontes de dados do Access entre **domínios** que, por padrão, desabilita o acesso entre domínios para formulários do InfoPath que residem nas zonas de segurança de **sites** restritos e da **Internet.** Essa configuração também solicita que o usuário permita ou não o acesso entre domínios para formulários do InfoPath que residem na zona de segurança da intranet local e permite o acesso entre domínios para formulários do InfoPath que residem nos **sites** confiáveis ou nas zonas do Computador **Local.**  
  
## <a name="malicious-use-of-activex-controls"></a>Uso mal-intencionado de controles ActiveX

O cenário principal para o uso mal-intencionado de controles ActiveX é quando um autor de formulário mal-intencionado grava código em um controle ActiveX que acessa o sistema de arquivos para recuperar arquivos pessoais e listas de senhas, excluir arquivos ou desabilitar o sistema do usuário. Um formulário do InfoPath pode executar código em controles ActiveX somente da lógica de negócios ou do script em execução em um painel de tarefas. O InfoPath não permite que scripts em exibições do InfoPath executem controles ActiveX.
  
O modelo de segurança do Internet Explorer no qual o InfoPath é criado fornece uma configuração chamada Inicializar e criar scripts de controles ActiveX marcados **como não seguros.** Essa configuração, por padrão, desabilita a inicialização e o script de controles ActiveX marcados como não seguros para formulários do InfoPath que residem na **intranet local,** **na Internet** e nas zonas de segurança de **sites** restritos. Ele solicita que o usuário permita ou não scripts de controles ActiveX marcados como não seguros para formulários do InfoPath que residem em **sites** confiáveis ou nas zonas de segurança do Computador **Local** e permite o script de controles ActiveX marcados como não seguros para formulários do InfoPath totalmente confiáveis. 
  
Além disso, você não pode inserir um controle ActiveX marcado como não seguro para inicialização e script no painel de tarefas de controles no modo de design, independentemente da zona de segurança em que você está ou do nível de confiança do formulário.
  
## <a name="malicious-use-of-infopath-object-model-code"></a>Uso mal-intencionado do código do modelo de objeto do InfoPath

Da mesma forma, os métodos e as propriedades do InfoPath chamados de código podem apresentar diferentes níveis de risco. Por exemplo, o método [SaveAs(String)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.SaveAs.aspx) da classe [XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) pode ser usado para gravar dados em qualquer local do sistema de arquivos. Para ajudar a proteger contra o uso mal-intencionado desses membros do modelo de objeto, o modelo de objeto do InfoPath implementa três níveis de segurança que determinam como e onde um determinado membro do modelo de objeto pode ser usado. Para obter mais informações sobre esse recurso, consulte [Sobre o modelo de segurança para modelos de formulário com código.](about-the-security-model-for-form-templates-with-code.md)
  
## <a name="best-practices-for-developers-of-infopath-forms"></a>Práticas recomendadas para desenvolvedores de formulários do InfoPath

Os desenvolvedores que criam formulários do InfoPath devem saber como implementar as seguintes práticas recomendadas de segurança:
  
- Como reconhecer possíveis problemas de segurança no arquivo XML associado a um formulário.
    
- Como evitar apresentar mensagens de erro confusas ou incômodas para os usuários do formulário.
    
- Como assinar os arquivos CAB dos controles ActiveX.
    
- Como assinar modelos de formulário enviados como anexos de uma mensagem de email.
    
## <a name="best-practices-for-xml-data-associated-with-a-form"></a>Práticas recomendadas para dados XML associados a um formulário

Observe que os formulários do InfoPath podem ser dados XML alimentados de qualquer fonte, incluindo aqueles em que o usuário não confia necessariamente ou controla. Por exemplo, o InfoPath pode obter dados XML de um link para uma página da Web ou de um anexo XML enviado ao usuário por email. Para reduzir esses riscos, esteja ciente das seguintes práticas recomendadas:
  
- Não passe dados não confiança lidos do XML para a função **eval()** do Microsoft JScript ou a propriedade **innerHTML** do painel de tarefas. Ambas as chamadas podem ser usadas para executar scripts mal-intencionados. Em um painel de tarefas, use a **propriedade innerText** como alternativa. Observe que as exibições do InfoPath não podem executar scripts. 
    
- Os dados enviados para um banco de dados a partir de um arquivo XML podem apresentar riscos de segurança ao banco de dados, caso não sejam validados antes do envio.
    
Os dados que não são validados antes de serem enviados a uma fonte de dados podem danificar a integridade dos dados na fonte de dados ou, em casos mais extremos, apresentar o potencial de sobrevavamentos de buffer. Também é possível causar injeção de script ou injeção SQL se você tentar usar dados não confiançados diretamente em seu servidor.
  
## <a name="best-practices-to-avoid-presenting-confusing-error-messages"></a>Práticas recomendadas para evitar apresentar mensagens de erro confusas

 **Implantar formulários e suas fontes de dados no mesmo domínio**
  
O risco de segurança do acesso a dados entre domínios não é claramente compreendido pela maioria dos usuários. A implantação de formulários que avisam e avisam continuamente os usuários sobre a permissão de acesso a dados entre domínios tem o efeito de treinar muitos usuários para aprovar todas as solicitações de acesso entre domínios ou adicionar o domínio de origem à sua lista de **sites** confiáveis, sem levar a sério os riscos de segurança. Para evitar essa situação, implante formulários do InfoPath no mesmo servidor das fontes de dados das quais dependem. 
  
 **Evite usar controles ActiveX que não estão marcados como seguros para scripts**
  
Os controles ActiveX podem expor propriedades e métodos que podem ser usados para comprometer o sistema de um usuário, como métodos para acessar o sistema de arquivos de um computador. Sempre que possível, você deve usar somente controles ActiveX marcados como seguros para scripts. Esses são controles que foram testados para garantir que eles não danificarão o sistema do usuário ou comprometerão a segurança do usuário, independentemente de como os métodos e as propriedades do controle são manipulados pelo script de uma página da Web. Da mesma forma, ao criar controles ActiveX para uso com o InfoPath, inspecione o código e teste o controle ActiveX rigorosamente antes de marcar como seguro para scripts.
  
O InfoPath usa um modelo de segurança baseado nas zonas de segurança do Internet Explorer. Portanto, um formulário do InfoPath usará as mesmas permissões que o Internet Explorer, que, por padrão, habilita chamadas de script para controles ActiveX marcados como seguros para script, sem solicitar aos usuários.
  
## <a name="best-practices-for-managing-the-cab-files-of-activex-controls"></a>Práticas recomendadas para gerenciar os arquivos CAB de controles ActiveX

Os controles ActiveX podem ser hospedados em modelos de formulário projetados para o editor do InfoPath. Arquivos CAB para esses controles que ainda não estão presentes no computador do usuário devem ser incluídos no arquivo de modelo de formulário (.xsn). Os arquivos CAB incluídos em modelos de formulário devem ser assinados digitalmente para que o arquivo CAB seja instalado. O InfoPath não instalará um arquivo CAB não assinado, independentemente do nível de confiança ou da zona de segurança.
  
Para garantir que a assinatura digital no arquivo CAB possa ser verificada, o arquivo deve ser assinado com um certificado que tenha uma cadeia de confiança, levando a uma raiz de certificado já confiável. Caso contrário, a assinatura não poderá ser autenticada, a verificação da assinatura falhará e o arquivo CAB não será instalado.
  
## <a name="best-practices-for-form-templates-sent-as-an-attachment-to-an-email-message"></a>Práticas recomendadas para modelos de formulário enviados como um anexo para uma mensagem de email

O InfoPath oferece suporte à implantação de modelos de formulário como um anexo a uma mensagem de email e à movimentação de modelos de formulário de um local para outro. É uma boa prática de segurança assinar digitalmente um modelo de formulário que você projeta e pretende implantar como um anexo para uma mensagem de email. Uma assinatura digital em um modelo de formulário implantado por mensagem de email não apenas garante a autenticidade do modelo. Ele também tem o benefício agregado de permitir que o modelo de formulário seja atualizado automaticamente.
  
O modelo de formulário deve ser assinado com um certificado que tenha uma cadeia de confiança, levando a uma raiz de certificado já confiável. Se ele não for assinado com esse certificado, a verificação de assinatura falhará, pois a assinatura não pode ser autenticada.
  
> [!NOTE]
> Se um modelo de formulário assinado solicitar acesso restrito ou domínio, o InfoPath não verificará ou verificará a assinatura, exceto para determinar se o InfoPath pode atualizar automaticamente o modelo. 
  
Você pode encontrar mais informações sobre a implantação de email em Níveis de Segurança, Implantação de Email e [Modelos de Formulário Remotos.](security-levels-email-deployment-and-remote-form-templates.md)
  

