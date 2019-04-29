---
title: Sobre o modelo de segurança para modelos de formulário com código
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
keywords:
- InfoPath 2007, segurança, segurança do acesso ao código [InfoPath 2007], segurança [InfoPath 2007], modelo de segurança para código gerenciado, segurança [InfoPath 2007], níveis, CAS [InfoPath 2007], modelos de formulário compatíveis com o InfoPath 2003, segurança, permissões [InfoPath 2007]
localization_priority: Normal
ms.assetid: 5e1c1c72-f98d-4871-9c57-82c315277aa1
description: Os modelos de formulário de código gerenciado do InfoPath dão suporte aos mesmos níveis de segurança que o script em execução em modelos de formulário não gerenciados, e também oferecem suporte a recursos de segurança de acesso a código adicionais que se aplicam ao código gerenciado em execução no CLR (Common Language Runtime) do. NET Framework.
ms.openlocfilehash: 97f0239a5bd6699b539ddaebf4d1d2ed7d1394db
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436143"
---
# <a name="about-the-security-model-for-form-templates-with-code"></a>Sobre o modelo de segurança para modelos de formulário com código

Os modelos de formulário de código gerenciado do InfoPath dão suporte aos mesmos níveis de segurança que o script em execução em modelos de formulário não gerenciados, e também oferecem suporte a recursos de segurança de acesso a código adicionais que se aplicam ao código gerenciado em execução no CLR (Common Language Runtime) do. NET Framework.
  
## <a name="infopath-managed-object-model-security-levels"></a>Níveis de segurança do modelo de objeto gerenciado do InfoPath

A tabela a seguir descreve a relação entre os níveis de segurança para membros do modelo de objeto de script e o conjunto de permissões correspondente que é exigido para cada nível quando o membro do modelo de objeto é usado em um modelo de formulário de código gerenciado.
  
|**Nível de segurança do modelo de objeto**|**Descrição**|**Conjunto de permissões exigido**|
|:-----|:-----|:-----|
|,0  <br/> |Podem ser acessados sem restrições.  <br/> |Nenhum  <br/> |
|duas  <br/> |Só pode ser acessado por formulários em execução no mesmo domínio que o formulário aberto atualmente ou por formulários que receberam permissões entre domínios.  <br/> |Nenhum  <br/> |
|3D  <br/> |Só pode ser acessado por formulários totalmente confiáveis.  <br/> |FullTrust  <br/> |
   
> [!NOTE]
> O nível de segurança "1" não é usado pelo servidor COM do InfoPath atual e está reservado para uso futuro. 
  
> [!IMPORTANT]
> Embora os níveis de modelo de objeto 0 e 2 não exijam qualquer conjunto de permissões, pois eles contêm código gerenciado, eles se comportam conforme definido para o nível de segurança de acesso ao domínio do domínio descrito na seção a seguir. 
  
O nível de segurança de cada membro de modelo de objeto exposto pelos assemblies Microsoft. Office. InfoPath e Microsoft. Office. Interop. InfoPath. SemiTrust é especificado na seção comentários do tópico que documenta o [membro no Namespaces Microsoft. Office. InfoPath](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) e [Microsoft. Office. Interop. InfoPath. SemiTrust](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.aspx) . 
  
## <a name="infopath-domain-access-security-levels"></a>Níveis de segurança de acesso ao domínio do InfoPath

Em conjunto com os níveis de segurança do modelo de objeto que são impostos pelo servidor COM exposto pelo aplicativo InfoPath, o InfoPath define três níveis de segurança que são aplicados dependendo de onde o modelo de formulário está localizado, como o formulário é implantado e configurações definidas no modo de design. Esses três níveis de segurança são definidos na tabela a seguir.
  
|**Nível de segurança de acesso ao domínio**|**Descrição**|
|:-----|:-----|
|Restrito  <br/> |Não permite qualquer comunicação fora do modelo de formulário. Este nível de segurança destina-se a evitar que formulários prejudiciais transmitam dados do seu computador para um invasor mal-intencionado. Ao executar nesse modo de segurança, os seguintes recursos não funcionarão: painel de tarefas personalizado, conexões de dados (exceto envio de email), controles ActiveX, código de formulário de código gerenciado, funções e fluxo de trabalho. Modelos de formulário de código gerenciado não podem ser executados no domínio restrito. Quando um modelo de formulário de código gerenciado é definido como a configuração de **nível de segurança determinar automaticamente** na categoria **segurança e confiança** da caixa de diálogo **Opções de formulário** , o modelo de formulário sempre exigirá pelo menos o acesso de segurança do domínio nível para executar o código.  <br/><br/>**Importante**: o assembly de código gerenciado criado para um modelo de formulário de código gerenciado não será carregado e executado quando um formulário for aberto a partir de um domínio restrito, por exemplo, de um formulário do InfoPath enviado como um anexo de email. Qualquer modelo de formulário que você deseja implantar como um anexo de email deve omitir os recursos listados acima e, se o modelo de formulário contiver código de formulário, o código de formulário deverá ser implementado em JScript ou VBScript e só deve usar membros do modelo de objeto com um nível de segurança 0 (zero) .           |
|Domínio  <br/> |Restringe um formulário com base em seu local em uma das zonas de segurança definidas pelo Microsoft Internet Explorer. Por exemplo, se o formulário estiver localizado na zona Intranet local, ele terá permissão para se comunicar com outros dados dentro de seu próprio domínio, mas não será permitido recuperar dados de outros domínios. O local em uma zona de segurança do Microsoft Internet Explorer também determina se os controles ActiveX marcados como não seguros para script poderão ser executados.  <br/> |
|Confiança Total  <br/> |Permite que você execute um formulário com confiança total no computador em que o formulário será usado. Este nível de segurança só pode ser usado ao trabalhar com um formulário assinado digitalmente com uma assinatura que corresponda a um fornecedor raiz confiável no seu computador ou criando um programa de instalação que instala o formulário e define o **requireFullTrust** atributo do elemento **xDocumentClass** como "Yes" no arquivo de definição de formulário (. xsf). Usando essa configuração, seu formulário pode acessar as chamadas de modelo de objeto que exigem o nível de segurança do modelo de objeto 3, como propriedades e métodos que acessam o sistema de arquivos, e você pode desabilitar determinados prompts de segurança que aparecem ao executar em uma segurança mais restritiva antes.  <br/> |
   
Por padrão, um formulário do InfoPath é configurado para selecionar automaticamente o nível de segurança restrito ou de domínio, dependendo dos recursos que estão sendo usados no modelo de formulário e onde e como o modelo de formulário é implantado. Por exemplo, um modelo de formulário implantado como anexo de email é automaticamente configurado para o nível de segurança restrito. A configuração de segurança é sempre mais restritiva possível, começando em restritos, para garantir um nível maior de proteção para você e seus dados. Quando um modelo de formulário que contém o código gerenciado é definido para selecionar automaticamente o nível de segurança, o modelo de formulário sempre precisará pelo menos do nível de acesso de segurança do domínio antes que o código possa ser executado. Você pode substituir manualmente essa configuração no tempo de design para selecionar um nível de segurança mais apropriado para o formulário usando o procedimento a seguir. 
  
### <a name="specify-a-forms-security-level"></a>Especificar o nível de segurança de um formulário

1. Abra o formulário no designer de formulários do InfoPath, clique na guia **arquivo** , em **informações**e em **Opções de formulário**.
    
2. Na caixa de diálogo **Opções de Formulário**, clique na categoria **Segurança e Confiabilidade**. 
    
3. DesMarque a caixa de seleção **determinar automaticamente o nível de segurança (recomendado)** . 
    
4. Escolha o nível de segurança desejado.
    
> [!NOTE] 
> - Se você selecionar o nível de segurança **restrito** para um modelo de formulário de código gerenciado, o código por trás do formulário não será carregado e executado independentemente de quais membros de modelo de objeto são usados no código de formulário. Este nível de segurança é projetado principalmente para formulários do InfoPath que são implantados usando email.     
> - Se você selecionar o nível de segurança de **confiança total** , deverá assinar ou instalar digitalmente e registrar o formulário. Para obter mais informações, consulte [implantar modelos de formulário do InfoPath com código](how-to-deploy-infopath-form-templates-with-code.md).
    
A tabela a seguir resume o modelo de segurança do InfoPath. A primeira coluna lista o nível especificado para ou exigido pelo formulário. A segunda e a terceira colunas especificam se o formulário tem um identificador URN ou de URL para seu local. As colunas restantes especificam o que pode ser executado. Para obter mais informações sobre cenários de implantação e conjuntos de permissões para modelos de formulário de código gerenciado, consulte a seção "recursos de segurança de acesso ao código do Common Language Runtime", mais adiante neste tópico.
  
|**Nível exigido pelo formulário**|**Tem identificador de URN**|**Tem um identificador de URL**|**ActiveX marcado como não seguro para scripts**|**Acesso entre domínios**|**Código gerenciado**|**Segurança do modelo de objeto**|
|:-----|:-----|:-----|:-----|:-----|:-----|:-----|
|Restrito  <br/> ||X  <br/> |Nenhum ActiveX é  <br/> |Malsucedida  <br/> |O formulário é carregado, mas o código gerenciado não é executado  <br/> |,0  <br/> |
|Domínio (zona de **sites restritos** do Internet Explorer)  <br/> |Não será executado de qualquer  <br/> |Não será executado de qualquer  <br/> |Não será executado de qualquer  <br/> |Não será executado de qualquer  <br/> |Não será executado de qualquer  <br/> |Não será executado de qualquer  <br/> |
|Domínio (zona **Internet** do Internet Explorer)  <br/> |X  <br/> ||Malsucedida  <br/> |Malsucedida  <br/> |Não será executado de qualquer  <br/> |,0  <br/> |
|Domínio (zona **intranet local** do Internet Explorer)  <br/> |X  <br/> ||Malsucedida  <br/> |Prompt  <br/> |O código gerenciado é executado com permissões de **intranet local** .  <br/> |duas  <br/> |
|Domínio (zona de **sites confiáveis** do Internet Explorer)  <br/> |X  <br/> ||Prompt  <br/> |OK  <br/> |O código gerenciado é executado com permissões de **Internet** . É permitido o acesso entre domínios. Observe que, embora o formulário esteja na zona **sites confiáveis** , as permissões de zona da **Internet** são aplicadas.  <br/> |duas  <br/> |
|Domínio (zona de **computador local** do Internet Explorer)  <br/> |X  <br/> |X  <br/> |Prompt  <br/> |Malsucedida  <br/> |O código gerenciado é executado com permissões de **intranet local** .  <br/> |duas  <br/> |
|Confiança Total  <br/> |X  <br/> |X  <br/> |OK  <br/> |OK  <br/> |Confiança Total  <br/> |3D  <br/> |
   
> [!IMPORTANT]
> As descrições acima nas colunas "o ActiveX marcou não é seguro para script" e "acesso entre domínios" pressupõem as configurações de segurança padrão para o Microsoft Internet Explorer. Se um usuário alterar suas configurações de segurança, o InfoPath se comportará de acordo. Por exemplo, se na zona **intranet local** , **acessar fontes de dados entre domínios** está definido como **habilitar**, os usuários não serão solicitados a permitir o acesso entre domínios, conforme descrito na tabela. 
  
## <a name="common-language-runtime-code-access-security-features"></a>Recursos de segurança de acesso a código do Common Language Runtime

Quando um modelo de formulário de código gerenciado do InfoPath é compilado, um assembly de código gerenciado privado é criado, contendo a implementação da lógica de código de formulário.
  
No .NET Framework, por padrão, um assembly de código gerenciado tem permissões de confiança total ao executar na máquina local e não recebe permissões de confiança total ao executar na intranet. Para fornecer controle mais refinado sobre a política de segurança e para fornecer a opção de executar modelos de formulário de código gerenciado do InfoPath como formulários totalmente confiáveis da intranet, o InfoPath implementa a seguinte arquitetura de segurança.
  
- O aplicativo InfoPath hospeda o CLR (Common Language Runtime) do .NET Framework.
    
- Dentro do CLR hospedado pelo InfoPath, cada modelo de formulário de código gerenciado é executado em um domínio de aplicativo separado, que é um ambiente que fornece isolamento, descarregamento e limites de segurança para executar código gerenciado.
    
- O InfoPath define uma política de segurança padrão no domínio do aplicativo, dependendo do nível de confiança associado ao modelo de formulário e a URL de sua localização.
    
- Por padrão, um modelo de formulário de código gerenciado em execução no computador local (o grupo de códigos de zona meu computador) Obtém um nível mais baixo de permissões do que confiança total (permissões de zona da intranet local). Para ter permissões de confiança total, o formulário deve ser registrado ou assinado digitalmente com um certificado confiável.
    
A política de segurança padrão definida para o domínio de aplicativo de um modelo de formulário de código gerenciado garante que os níveis de segurança do acesso ao domínio do InfoPath, bem como quaisquer restrições de segurança adicionais do .NET, sejam aplicados. Para fornecer flexibilidade adicional, o sistema de segurança do InfoPath reconhece um grupo de códigos de segurança do acesso ao código .NET chamado "modelos de formulário do InfoPath". Se esse grupo de códigos estiver presente no computador de um usuário, sua configuração de segurança e os de qualquer grupo de códigos filho dentro dele serão aplicados ao domínio do aplicativo.
  
> [!IMPORTANT] 
> - O grupo de códigos de modelos de formulário do InfoPath aplica-se somente ao assembly de código de formulário de código gerenciado. Como resultado, se você conceder o conjunto de permissões de confiança total ao código de formulário de código gerenciado do InfoPath, mas não tiver instalado e registrado (ou assinado digitalmente) o próprio modelo de formulário (que torna todo o modelo de formulário totalmente confiável), as chamadas no código de formulário para segurança os membros do modelo de objeto Level 3 ainda falharão.   
> - Se você referenciar ou carregar explicitamente (assembly. Load) um assembly que é configurado com um conjunto de permissões restritos usando hash, nome forte ou evidência do Publisher para determinar sua condição de associação em um projeto de modelo de formulário, o assembly mesmo assim será carregado e executado pelo modelo de formulário.
    
Para obter informações sobre como criar e configurar o grupo de códigos de modelos de formulário do InfoPath, consulte [definir configurações de segurança para modelos de formulário com código](how-to-configure-security-settings-for-form-templates-with-code.md).
  
A tabela a seguir resume os cenários de implantação e os conjuntos de permissões que se aplicam a modelos de formulário de código gerenciado.
  
|**Cenário de implantação**|**Conjunto de permissões**|**Anotações**|
|:-----|:-----|:-----|
|O modelo de formulário é publicado no computador local e o desenvolvedor está usando o Visual Studio para escrever e depurar o código de formulário.  <br/> |Conjunto de permissões de intranet local.  <br/> Assemblies instalados no cache de assembly global (GAC) e marcados com o atributo **AllowPartiallyTrustedCallersAttribute** recebem o conjunto de permissões de confiança total.  <br/> |Por padrão, os modelos de formulário em execução no computador local não recebem o conjunto de permissões de confiança total. Ao desenvolver modelos de formulário que usam recursos e chamadas para membros do modelo de objeto que exigem permissões de confiança total, você pode usar o procedimento descrito nos [modelos de formulário Visualizar e depurar que exigem confiança total](how-to-preview-and-debug-form-templates-that-require-full-trust.md).  <br/> |
|O modelo de formulário é publicado no computador local e faz referência a um assembly personalizado que solicita o conjunto de permissões de confiança total no computador local.  <br/> |Conjunto de permissões de intranet local.  <br/> Assemblies instalados no cache de assembly global (GAC) e marcados com o atributo **AllowPartiallyTrustedCallersAttribute** recebem o conjunto de permissões de confiança total. O conjunto de permissões de intranet local é concedido ao assembly personalizado.  <br/> |Para fazer referência a assemblies externos para uso no código do modelo de formulário, o desenvolvedor deve usar o grupo de códigos modelos de formulário do InfoPath para conceder confiança total (ou o conjunto de permissões apropriado) ao assembly externo referenciado no código do modelo de formulário. O InfoPath não faz suposições sobre assemblies externos diferentes daqueles instalados no cache de assembly global (GAC). O desenvolvedor deve conceder explicitamente ao assembly as permissões necessárias usando o grupo de código modelos de formulário do InfoPath, mesmo que o assembly já seja confiável, embora permissões concedidas no grupo de códigos My_Computer_Zone.  <br/> |
|O modelo de formulário é publicado em um local compartilhado na intranet local, como um compartilhamento de arquivos, uma biblioteca de formulários do SharePoint ou um servidor Web.  <br/> |Conjunto de permissões de intranet local.  <br/> Assemblies instalados no cache de assembly global (GAC) e marcados com o atributo **AllowPartiallyTrustedCallersAttribute** recebem o conjunto de permissões de confiança total.  <br/> ||
|O modelo de formulário é publicado em um local compartilhado na intranet local, como um compartilhamento de arquivos, uma biblioteca de formulários do SharePoint ou um servidor Web designado como um site confiável no Internet Explorer.  <br/> |Conjunto de permissões de Internet.  <br/> Assemblies assinados pela Microsoft e pela ECMA recebem o conjunto de permissões de confiança total.  <br/> |A segurança do acesso ao código CLR concede apenas o conjunto de permissões da Internet aos sites designados como sites confiáveis no Internet Explorer. O InfoPath respeita essa política. Observe que isso é diferente de um modelo de formulário do InfoPath que usa script para o código de formulário, que recebe um nível mais alto de permissões quando é publicado em uma zona de sites confiáveis.  <br/> |
|O modelo de formulário é baixado ou copiado de um local da Internet.  <br/> |Por padrão, nenhum. O assembly de código gerenciado para o modelo de formulário não é carregado e não é executado.  <br/> ||
   
## <a name="see-also"></a>Confira também

- [Definir configurações de segurança para modelos de formulário com código](how-to-configure-security-settings-for-form-templates-with-code.md)
- [Visualizar e depurar modelos de formulário que exigem confiança total](how-to-preview-and-debug-form-templates-that-require-full-trust.md)

