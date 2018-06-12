---
title: Sobre o modelo de segurança para modelos de formulário com código
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
keywords:
- InfoPath 2007, segurança, segurança de acesso do código [InfoPath 2007], [InfoPath 2007] de segurança, o modelo de segurança para o código gerenciado, segurança [InfoPath 2007], níveis, CAS [InfoPath 2007], modelos de formulário compatíveis com o InfoPath 2003, segurança, permissões [InfoPath 2007]
localization_priority: Normal
ms.assetid: 5e1c1c72-f98d-4871-9c57-82c315277aa1
description: Suporte de modelos de formulário de código a mesma segurança redistribui como script em execução nos modelos de formulário não gerenciadas de gerenciado do InfoPath e também dão suporte a recursos de segurança de acesso de código adicionais que se aplicam ao código gerenciado executadas sob o common language runtime (CLR) dos. NET Framework.
ms.openlocfilehash: cfeb2117232d041cef43d282ff5aab482609f512
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765592"
---
# <a name="about-the-security-model-for-form-templates-with-code"></a>Sobre o modelo de segurança para modelos de formulário com código

Suporte de modelos de formulário de código a mesma segurança redistribui como script em execução nos modelos de formulário não gerenciadas de gerenciado do InfoPath e também dão suporte a recursos de segurança de acesso de código adicionais que se aplicam ao código gerenciado executadas sob o common language runtime (CLR) dos. NET Framework.
  
## <a name="infopath-managed-object-model-security-levels"></a>Níveis de segurança do modelo de objeto de gerenciado do InfoPath

A tabela a seguir descreve a relação entre os níveis de segurança para membros do modelo de objeto de script e o conjunto de permissões correspondente que é exigido para cada nível quando o membro de modelo de objeto é usado em um modelo de formulário de código gerenciado.
  
|**Nível de segurança do modelo de objeto**|**Descrição**|**Permissão definida usado**|
|:-----|:-----|:-----|
|0  <br/> |Pode ser acessado sem restrições.  <br/> |None  <br/> |
|2  <br/> |Pode ser acessado apenas por formulários sendo executados no mesmo domínio que o formulário atualmente aberto ou por formulários que receberam permissões entre domínios.  <br/> |None  <br/> |
|3  <br/> |Pode ser acessado apenas por formulários totalmente confiáveis.  <br/> |FullTrust  <br/> |
   
> [!NOTE]
> O nível de segurança "1" não é usado pelo servidor atual COM o InfoPath e está reservado para uso futuro. 
  
> [!IMPORTANT]
> Embora os níveis de modelo de objeto 0 e 2 não exigem qualquer conjunto de permissões, porque eles contêm código gerenciado, elas se comportam conforme definido para o nível de segurança de acesso de domínio do domínio que é descrito na seção a seguir. 
  
O nível de segurança de cada membro de modelo de objeto exposto pelos assemblies Microsoft.Office.InfoPath e SemiTrust é especificado na seção comentários do tópico que documenta esse membro no [ Microsoft.Office.InfoPath](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) e namespaces [SemiTrust](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.aspx) . 
  
## <a name="infopath-domain-access-security-levels"></a>Níveis de segurança de acesso do domínio do InfoPath

Em conjunto com os níveis de segurança do modelo de objeto que são impostas pelo servidor COM expostos pelo aplicativo InfoPath, InfoPath define três níveis de segurança que são aplicados dependendo de onde o modelo de formulário está localizado, como o formulário é implantado, e definições configuradas no modo de design. Esses três níveis de segurança são definidos na tabela a seguir.
  
|**Nível de segurança de acesso do domínio**|**Descrição**|
|:-----|:-----|
|Restrito  <br/> |Não permitir que qualquer comunicação fora o modelo de formulário. Esse nível de segurança é destinado a impedir a transmissão de dados do seu computador para um invasor mal-intencionado formulários prejudiciais. Ao executar neste modo de segurança, os seguintes recursos não funcionará: o painel de tarefas personalizado, conexões de dados (exceto o envio de email), os controles ActiveX, código de formulário de código gerenciado, funções e fluxo de trabalho. Gerenciados não podem ser executado no domínio restrito modelos de formulário de código. Quando um modelo de formulário de código gerenciado é definido como a configuração de **determinar o nível de segurança automaticamente** na categoria de **segurança e confiança** da caixa de diálogo **Opções de formulário** , o modelo de formulário sempre exigirá pelo menos o acesso de segurança de domínio nível para executar um código.  <br/><br/>**Importante**: O assembly de código gerenciado criado para um modelo de formulário de código gerenciado não vai ser carregado e executado quando um formulário é aberto a partir de um domínio restrito, por exemplo, a partir de um formulário do InfoPath enviado como um anexo de email. Qualquer modelo de formulário que você deseja implantar como um anexo de email deve omitir os recursos listados acima, e se o modelo de formulário contém código de formulário, o código de formulário deve ser implementado em JScript ou VBScript e deve utilizar apenas os membros do modelo de objeto com um nível de segurança de 0 (zero) .           |
|Domínio  <br/> |Restringe a um formulário baseado em seu local em uma das zonas de segurança definidas pelo Microsoft Internet Explorer. Por exemplo, se o formulário está localizado na zona da Intranet Local, ele pode se comunicar com outros dados dentro de seu próprio domínio, mas não é permitido para recuperar dados de outros domínios. O local em uma zona de segurança do Microsoft Internet Explorer também determina se os controles ActiveX que são marcados como seguros para script terão permissão para executar.  <br/> |
|Confiança total  <br/> |Permite a execução de um formulário com confiança total no computador onde o formulário será usado. Esse nível de segurança só pode ser usado ao trabalhar com um formulário que é assinado digitalmente com uma assinatura que corresponde a um fornecedor de raiz confiável no seu computador ou criando um programa de instalação que instala o formulário e define o **requireFullTrust** atributo do elemento **xDocumentClass** como "yes" no arquivo de definição de formulário (. xsf). Usando essa configuração, seu formulário pode acessar as chamadas de modelo de objeto que exigem o nível de segurança de modelo objeto 3, como propriedades e métodos que acessam o sistema de arquivos, e você pode desabilitar determinados avisos de segurança que aparecem durante a execução em um título mais restritivo nível.  <br/> |
   
Por padrão, um formulário do InfoPath é configurado para selecione automaticamente o nível de segurança de domínio ou restrito dependendo dos recursos que estão sendo usados no modelo de formulário, e onde e como o modelo de formulário é implantado. Por exemplo, um modelo de formulário implantado como um anexo de email é configurado automaticamente o nível de segurança restrito. A configuração de segurança é tão restritiva sempre que possível, começando restrito, para garantir um maior nível de proteção para você e seus dados. Quando um modelo de formulário que contém o código gerenciado é definido para selecionar automaticamente o nível de segurança, o modelo de formulário sempre exigirá pelo menos o nível de acesso de segurança de domínio antes de código pode ser executado. Manualmente, você pode substituir essa configuração no tempo de design para selecionar um nível de segurança que é mais apropriado para o formulário usando o procedimento a seguir. 
  
### <a name="specify-a-forms-security-level"></a>Especificar o nível de segurança de um formulário

1. Abra o formulário no designer de formulários do InfoPath, clique na guia **arquivo** , clique em **Info**e, em seguida, clique em **Opções de formulário**.
    
2. Na caixa de diálogo **Opções de formulário** , clique na categoria de **segurança e confiança** . 
    
3. Limpar o **determinar o nível de segurança automaticamente (recomendado)** caixa de seleção. 
    
4. Selecione o nível de segurança desejado.
    
> [!NOTE] 
> - Se você selecionar o nível de segurança para um modelo de formulário de código gerenciado, o código por trás do formulário **restrito** não será carregado e executado independentemente de qual objeto membros de modelo são usados no código do formulário. Esse nível de segurança destina-se principalmente para formulários do InfoPath que são implantados usando email.     
> - Se você selecionar o nível de segurança **Confiança total** , você precisará assinar digitalmente ou instalar e registrar o formulário. Para obter mais informações, consulte [Implantar modelos de formulário do InfoPath com código](how-to-deploy-infopath-form-templates-with-code.md).
    
A tabela a seguir resume o modelo de segurança do InfoPath. A primeira coluna lista o nível especificado para ou necessários para o formulário. As colunas de segunda e terceira especificam se o formulário tem um identificador URN ou uma URL para seu local. As colunas remanescentes especificam o que pode ser executado. Para obter mais informações sobre a implantação de permissão e cenários define para modelos de formulário de código gerenciado, consulte a seção "Common Language Runtime código acesso recursos de segurança" mais adiante neste tópico.
  
|**Nível exigido por formulário**|**Tem URN identificador**|**Tem um identificador de URL**|**ActiveX marcados não seguro para scripts**|**Acesso entre domínios**|**Código gerenciado**|**Segurança do modelo de objeto**|
|:-----|:-----|:-----|:-----|:-----|:-----|:-----|
|Restricted  <br/> ||X  <br/> |Nenhum ActiveX mudaram  <br/> |Falhar  <br/> |Formar cargas, mas gerenciada código não serão executados  <br/> |0  <br/> |
|Domínio (zona **sites restritos** do Internet Explorer)  <br/> |Não é executada  <br/> |Não é executada  <br/> |Não é executada  <br/> |Não é executada  <br/> |Não é executada  <br/> |Não é executada  <br/> |
|Domínio (zona da Internet Explorer **Internet** )  <br/> |X  <br/> ||Falhar  <br/> |Falhar  <br/> |Não é executada  <br/> |0  <br/> |
|Domínio (zona da Internet Explorer **intranet Local** )  <br/> |X  <br/> ||Falhar  <br/> |Prompt  <br/> |Código gerenciado é executado com permissões de **intranet Local** .  <br/> |2  <br/> |
|Domínio (zona **sites confiáveis** do Internet Explorer)  <br/> |X  <br/> ||Prompt  <br/> |OK  <br/> |Código gerenciado é executado com permissões de **Internet** . Acesso entre domínios é permitido. Observe que, mesmo que o formulário está na zona **sites confiáveis** , permissões de zona da **Internet** sejam aplicadas.  <br/> |2  <br/> |
|Domínio (zona da Internet Explorer **computador Local** )  <br/> |X  <br/> |X  <br/> |Prompt  <br/> |Falhar  <br/> |Código gerenciado é executado com permissões de **intranet Local** .  <br/> |2  <br/> |
|Confiança total  <br/> |X  <br/> |X  <br/> |OK  <br/> |OK  <br/> |Confiança total  <br/> |3  <br/> |
   
> [!IMPORTANT]
> Descrições acima o "ActiveX marcados não seguro para script" e colunas de "Acesso entre domínios" pressupõem o padrão de configurações de segurança para o Microsoft Internet Explorer. Se um usuário alterar suas configurações de segurança, InfoPath irá se comportar adequadamente. Por exemplo, se na zona **da intranet Local** , **acessar fontes de dados entre domínios** estiver definida como **Habilitar**, e em seguida, os usuários não serão solicitados para permitir acesso entre domínios como descrito na tabela. 
  
## <a name="common-language-runtime-code-access-security-features"></a>Comuns recursos de segurança do acesso em tempo de execução de código de idioma

Quando um modelo de formulário de código gerenciado é compilado de InfoPath, um assembly de código gerenciado privada é criado que contém a implementação da lógica de código do formulário.
  
No .NET Framework, por padrão, um assembly de código gerenciado tem permissões de confiança total durante a execução na máquina local e não está concedidas permissões de confiança total ao executar na Intranet. Para fornecer mais controle refinado sobre diretiva de segurança e para oferecer a opção para executar o código gerenciado do InfoPath modelos de formulário como formulários totalmente confiáveis da Intranet, o InfoPath implementa a arquitetura de segurança a seguir.
  
- O aplicativo InfoPath hospeda o .NET Framework common language runtime (CLR).
    
- Dentro do CLR hospedado pelo InfoPath, cada modelo de formulário de código gerenciado é executado em um domínio de aplicativo separado, que é um ambiente que fornece isolamento, descarregar, e os limites de segurança para a execução de código gerenciado.
    
- InfoPath define uma diretiva de segurança padrão no domínio do aplicativo, dependendo do nível de confiança associado com o modelo de formulário e a URL do seu local.
    
- Por padrão, um modelo de formulário de código gerenciado em execução no computador local (o grupo de códigos de zona do meu computador) obtém um nível inferior das permissões de confiança total (permissões de zona da Intranet Local). Para ter permissões de confiança total, o formulário deve ser registrado ou assinado digitalmente com um certificado confiável.
    
A diretiva de segurança padrão definido para o domínio de aplicativo de um modelo de formulário de código gerenciado garante que os níveis de segurança de acesso de domínio do InfoPath, bem como qualquer restrição de segurança do .NET adicionais é impostas. Para fornecer flexibilidade adicional, o sistema de segurança do InfoPath reconhece um .NET código acesso segurança código grupo chamado "Modelos de formulário do InfoPath". Se este grupo de códigos estiver presente no computador de um usuário, a configuração de segurança e as de quaisquer grupos de códigos filho dentro dele serão aplicada ao domínio do aplicativo.
  
> [!IMPORTANT] 
> - O grupo de códigos de modelos de formulário do InfoPath só se aplica ao assembly de código de formulário de código gerenciado em si. Como resultado, se você conceder a permissão de confiança total definida como InfoPath código formulário código gerenciado, mas você não tiver instalado e registrado (ou assinada digitalmente) o modelo de formulário em si (que faz com que o modelo de formulário inteiro totalmente confiável), chama no código do formulário para segurança membros do modelo de objeto de nível 3 ainda falhará.   
> - Se você referenciar ou carregar explicitamente (Load) de um assembly que é configurado com uma permissão restrita definida usando Hash, nome forte ou evidência do Publisher para determinar sua condição de associação em um projeto de modelo de formulário, o assembly, mesmo assim, será carregado e executado pelo modelo de formulário.
    
Para obter informações sobre como criar e configurar o grupo de códigos de modelos de formulário do InfoPath, consulte [Configurar definições de segurança para modelos de formulário com código](how-to-configure-security-settings-for-form-templates-with-code.md).
  
A tabela a seguir resume os cenários de implantação e os conjuntos de permissões que se aplicam aos modelos de formulário de código gerenciado.
  
|**Cenário de implantação**|**Conjunto de permissões**|**Notes**|
|:-----|:-----|:-----|
|O modelo de formulário é publicado no computador local, e o desenvolvedor está usando o Visual Studio para escrever e depurar código do formulário.  <br/> |Conjunto de permissões de Intranet local.  <br/> Assemblies instalados no Cache de Assembly Global (GAC) e marcados com o atributo **AllowPartiallyTrustedCallersAttribute** recebem o conjunto de permissões de confiança total.  <br/> |Por padrão, os modelos de formulário executando a partir do computador local não recebem o conjunto de permissões de confiança total. Enquanto os membros que exigem permissões de confiança total do modelo de desenvolver modelos de formulário que usam os recursos e as chamadas para o objeto, você pode usar o procedimento descrito em [Visualizar e depurar modelos de formulário que exigem confiança total](how-to-preview-and-debug-form-templates-that-require-full-trust.md).  <br/> |
|O modelo de formulário é publicado no computador local e faz referência a um assembly personalizado que solicita a permissão de confiança total definida no computador local.  <br/> |Conjunto de permissões de Intranet local.  <br/> Assemblies instalados no Cache de Assembly Global (GAC) e marcados com o atributo **AllowPartiallyTrustedCallersAttribute** recebem o conjunto de permissões de confiança total. O assembly personalizado recebe o conjunto de permissões de Intranet Local.  <br/> |Para fazer referência a assemblies externos para uso em código do modelo de formulário, o desenvolvedor deve usar o grupo de códigos de modelos de formulário do InfoPath para conceder confiança total (ou o conjunto de permissões apropriado) para o assembly externo mencionado no código do modelo de formulário. InfoPath não faz suposições sobre assemblies externos além daquelas instalado no Cache de Assembly Global (GAC). O desenvolvedor deve conceder explicitamente o assembly as permissões necessárias usando o grupo de códigos de modelos de formulário do InfoPath, mesmo se o assembly já foi entanto confiáveis permissões concedidas no grupo código, My_Computer_Zone.  <br/> |
|O modelo de formulário é publicado em um local compartilhado na intranet local, como um compartilhamento de arquivos, biblioteca de formulários do SharePoint ou um servidor Web.  <br/> |Conjunto de permissões de Intranet local.  <br/> Assemblies instalados no Cache de Assembly Global (GAC) e marcados com o atributo **AllowPartiallyTrustedCallersAttribute** recebem o conjunto de permissões de confiança total.  <br/> ||
|O modelo de formulário é publicado em um local compartilhado na intranet local, como um compartilhamento de arquivos, biblioteca de formulários do SharePoint ou um servidor Web que é designado como um site confiáveis no Internet Explorer.  <br/> |Conjunto de permissões de Internet.  <br/> Assemblies assinados pela Microsoft e ECMA recebem o conjunto de permissões de confiança total.  <br/> |Segurança de acesso do código CLR concede somente Internet conjunto de permissões para sites que forem designados como sites confiáveis no Internet Explorer. InfoPath respeita essa diretiva. Observe que isso é diferente de um modelo de formulário do InfoPath que usa o script para o código de formulário, que recebe um nível mais alto de permissões quando publicado em uma zona de sites confiáveis.  <br/> |
|O modelo de formulário é baixado ou copiado de um local da Internet.  <br/> |Por padrão, nenhum. O assembly de código gerenciado para o modelo de formulário não é carregado e não é executado.  <br/> ||
   
## <a name="see-also"></a>Confira também

- [Definir configurações de segurança para modelos de formulário com código](how-to-configure-security-settings-for-form-templates-with-code.md)
- [Visualizar e depurar os modelos de formulário que exijam confiança total](how-to-preview-and-debug-form-templates-that-require-full-trust.md)

