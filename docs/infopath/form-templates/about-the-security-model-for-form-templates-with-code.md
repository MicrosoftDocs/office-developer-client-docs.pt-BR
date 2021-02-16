---
title: Sobre o modelo de segurança para modelos de formulário com código
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
keywords:
- infopath 2007, segurança, segurança de acesso ao código [InfoPath 2007], segurança [InfoPath 2007], modelo de segurança para código gerenciado, segurança [InfoPath 2007], níveis,CAS [InfoPath 2007],modelos de formulário compatíveis com o InfoPath 2003, segurança, permissões [InfoPath 2007]
localization_priority: Normal
ms.assetid: 5e1c1c72-f98d-4871-9c57-82c315277aa1
description: Os modelos de formulário de código gerenciado do InfoPath suportam os mesmos níveis de segurança que o script executado em modelos de formulário não gerenciados e também suportam recursos adicionais de segurança de acesso a código que se aplicam ao código gerenciado em execução no CLR (Common Language Runtime) do .NET Framework.
ms.openlocfilehash: 97f0239a5bd6699b539ddaebf4d1d2ed7d1394db
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436143"
---
# <a name="about-the-security-model-for-form-templates-with-code"></a>Sobre o modelo de segurança para modelos de formulário com código

Os modelos de formulário de código gerenciado do InfoPath suportam os mesmos níveis de segurança que o script executado em modelos de formulário não gerenciados e também suportam recursos adicionais de segurança de acesso a código que se aplicam ao código gerenciado em execução no CLR (Common Language Runtime) do .NET Framework.
  
## <a name="infopath-managed-object-model-security-levels"></a>Níveis de segurança do modelo de objeto gerenciado do InfoPath

A tabela a seguir descreve a relação entre os níveis de segurança para membros do modelo de objeto de script e o conjunto de permissões correspondente que é exigido para cada nível quando o membro do modelo de objeto é usado em um modelo de formulário de código gerenciado.
  
|**Nível de segurança do modelo de objeto**|**Descrição**|**Conjunto de Permissões Exigido**|
|:-----|:-----|:-----|
|0  <br/> |Pode ser acessado sem restrições.  <br/> |Nenhum  <br/> |
|2   <br/> |Pode ser acessado somente por formulários em execução no mesmo domínio que o formulário aberto no momento ou por formulários que foram concedidos com permissões entre domínios.  <br/> |Nenhum  <br/> |
|3   <br/> |Pode ser acessado somente por formulários totalmente confiáveis.  <br/> |FullTrust  <br/> |
   
> [!NOTE]
> O nível de segurança "1" não é usado pelo servidor COM atual do InfoPath e é reservado para uso futuro. 
  
> [!IMPORTANT]
> Embora os níveis 0 e 2 do modelo de objeto não exijam nenhum conjunto de permissões, pois contêm código gerenciado, eles se comportam como definidos para o nível de segurança de acesso de domínio do domínio descrito na seção a seguir. 
  
O nível de segurança de cada membro do modelo de objeto exposto pelos assemblies Microsoft.Office.InfoPath e Microsoft.Office.Interop.InfoPath.SemiTrust é especificado na seção Comentários do tópico que documenta esse membro nos namespaces [Microsoft.Office.InfoPath](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) e [Microsoft.Office.Interop.InfoPath.SemiTrust.](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.aspx) 
  
## <a name="infopath-domain-access-security-levels"></a>Níveis de segurança de acesso de domínio do InfoPath

Em conjunto com os níveis de segurança do modelo de objeto imposto pelo servidor COM exposto pelo aplicativo InfoPath, o InfoPath define três níveis de segurança que são aplicados dependendo de onde o modelo de formulário está localizado, como o formulário é implantado e configurações definidas no modo de design. Esses três níveis de segurança são definidos na tabela a seguir.
  
|**Nível de segurança de acesso de domínio**|**Descrição**|
|:-----|:-----|
|Restrito  <br/> |Não permite nenhuma comunicação fora do modelo de formulário. Este nível de segurança destina-se a evitar que formulários prejudiciais transmitam dados do seu computador para um invasor mal-intencionado. Ao executar nesse modo de segurança, os seguintes recursos não funcionarão: Painel de Tarefas Personalizado, Conexões de Dados (exceto envio de email), controles ActiveX, código de formulário de código gerenciado, Funções e Fluxo de Trabalho. Os modelos de formulário de código gerenciado não podem ser executados no domínio Restrito. Quando um modelo de formulário de código gerenciado é  definido para determinar  automaticamente a configuração de nível de segurança na categoria Segurança e Confiança da caixa de diálogo Opções de Formulário, o modelo de formulário sempre exigirá pelo menos o nível de acesso de segurança domínio para executar código.   <br/><br/>**IMPORTANTE:** o assembly de código gerenciado criado para um modelo de formulário de código gerenciado não será carregado e executado quando um formulário for aberto a partir de um domínio restrito, por exemplo, de um formulário do InfoPath enviado como um anexo de email. Qualquer modelo de formulário que você deseja implantar como um anexo de email deve omitir os recursos listados acima e, se o modelo de formulário contiver código de formulário, o código de formulário deverá ser implementado em JScript ou VBScript e deverá utilizar apenas membros do modelo de objeto com um nível de segurança 0 (zero).           |
|Domínio  <br/> |Restringe um formulário com base em sua localização em uma das zonas de segurança definidas pelo Microsoft Internet Explorer. Por exemplo, se o formulário estiver localizado na zona da Intranet Local, ele poderá se comunicar com outros dados dentro de seu próprio domínio, mas não poderá recuperar dados de outros domínios. O local em uma zona de segurança do Microsoft Internet Explorer também determina se os controles ActiveX marcados como não seguros para script poderão ser executados.  <br/> |
|Confiança Total  <br/> |Permite que você execute um formulário com confiança total no computador onde o formulário será usado. Esse nível de segurança só pode ser usado ao trabalhar com um formulário assinado digitalmente com uma assinatura que corresponde a um editor raiz confiável em seu computador ou criando um programa de instalação que instala o formulário e define o atributo **requireFullTrust** do elemento **xDocumentClass** como "sim" no arquivo de definição de formulário (.xsf). Usando essa configuração, seu formulário pode acessar chamadas de modelo de objeto que exigem o nível de segurança 3 do modelo de objeto, como propriedades e métodos que acessam o sistema de arquivos, e você pode desabilitar determinados prompts de segurança que aparecem quando executados em um nível de segurança mais restritivo.  <br/> |
   
Por padrão, um formulário do InfoPath é configurado para selecionar automaticamente o nível de segurança Restrito ou domínio, dependendo dos recursos que estão sendo usados no modelo de formulário, e onde e como o modelo de formulário é implantado. Por exemplo, um modelo de formulário implantado como um anexo de email é configurado automaticamente para o nível de segurança Restrito. A configuração de segurança é sempre o mais restritiva possível, começando em Restrito, para garantir um nível maior de proteção para você e seus dados. Quando um modelo de formulário que contém código gerenciado é definido para selecionar automaticamente o nível de segurança, o modelo de formulário sempre exigirá pelo menos o nível de acesso de segurança domínio antes que o código possa ser executado. You can manually override this setting at design time to select a level of security that is more appropriate for the form by using the following procedure. 
  
### <a name="specify-a-forms-security-level"></a>Especificar o nível de segurança de um formulário

1. Abra o formulário no designer de  formulário do InfoPath, clique na guia Arquivo, em **Informações** e em Opções **de Formulário.**
    
2. Na caixa de diálogo **Opções de Formulário**, clique na categoria **Segurança e Confiabilidade**. 
    
3. Des **marque a caixa de seleção Determinar automaticamente o nível de** segurança (recomendado). 
    
4. Escolha o nível de segurança desejado.
    
> [!NOTE] 
> - Se você selecionar  o nível de segurança Restrito para um modelo de formulário de código gerenciado, o código por trás do formulário não será carregado e executado independentemente de quais membros do modelo de objeto são usados no código do formulário. Esse nível de segurança foi projetado principalmente para formulários do InfoPath implantados usando email.     
> - Se você selecionar o **nível de segurança** Confiança Total, precisará assinar digitalmente ou instalar e registrar o formulário. Para obter mais informações, [consulte Implantar modelos de formulário do InfoPath com código.](how-to-deploy-infopath-form-templates-with-code.md)
    
A tabela a seguir resume o modelo de segurança do InfoPath. A primeira coluna lista o nível especificado ou exigido pelo formulário. A segunda e a terceira colunas especificam se o formulário tem um identificador URN ou URL para seu local. As colunas restantes especificam o que pode ser executado. Para obter mais informações sobre cenários de implantação e conjuntos de permissões para modelos de formulário de código gerenciado, consulte a seção "Common Language Runtime Code Access Security Features" posteriormente neste tópico.
  
|**Nível exigido por formulário**|**Tem identificador URN**|**Tem identificador de URL**|**ActiveX marcado como não seguro para script**|**Acesso entre domínios**|**Código gerenciado**|**Segurança do modelo de objeto**|
|:-----|:-----|:-----|:-----|:-----|:-----|:-----|
|Restrito  <br/> ||X  <br/> |Nenhum ActiveX  <br/> |Falha  <br/> |O formulário é carregado, mas o código gerenciado não é executado  <br/> |0  <br/> |
|Domínio (zona de **sites restritos do** Internet Explorer)  <br/> |Não será executado  <br/> |Não será executado  <br/> |Não será executado  <br/> |Não será executado  <br/> |Não será executado  <br/> |Não será executado  <br/> |
|Domínio (zona internet do **Internet** Explorer)  <br/> |X  <br/> ||Falha  <br/> |Falha  <br/> |Não será executado  <br/> |0  <br/> |
|Domínio (zona **da intranet local do** Internet Explorer)  <br/> |X  <br/> ||Falha  <br/> |Prompt  <br/> |O código gerenciado é executado **com permissões de intranet** local.  <br/> |2   <br/> |
|Domínio (zona de **sites confiáveis do** Internet Explorer)  <br/> |X  <br/> ||Prompt  <br/> |OK  <br/> |O código gerenciado é executado com permissões da **Internet.** O acesso entre domínios é permitido. Observe que, embora o formulário está na zona **sites confiáveis,** as permissões de zona da **Internet** são aplicadas.  <br/> |2   <br/> |
|Domínio (zona do computador **local do** Internet Explorer)  <br/> |X  <br/> |X  <br/> |Prompt  <br/> |Falha  <br/> |O código gerenciado é executado **com permissões de intranet** local.  <br/> |2   <br/> |
|Confiança Total  <br/> |X  <br/> |X  <br/> |OK  <br/> |OK  <br/> |Confiança Total  <br/> |3   <br/> |
   
> [!IMPORTANT]
> As descrições acima nas colunas "ActiveX marcado como não seguro para script" e "Acesso entre Domínios" assumem as configurações de segurança padrão do Microsoft Internet Explorer. Se um usuário mudar suas configurações de segurança, o InfoPath se comportará de acordo. Por exemplo, se na zona da **intranet local,** as fontes de dados do Access entre domínios estão definidas como Habilitar, os usuários não serão solicitados a permitir o acesso entre **domínios,** conforme descrito na tabela. 
  
## <a name="common-language-runtime-code-access-security-features"></a>Common Language Runtime Code Access Security Features

Quando um modelo de formulário de código gerenciado do InfoPath é compilado, um assembly de código gerenciado privado é criado contendo a implementação da lógica de código do formulário.
  
No .NET Framework, por padrão, um assembly de código gerenciado tem permissões de Confiança Total ao ser executado no computador local e não recebe permissões de Confiança Total durante a execução na Intranet. Para fornecer um controle mais preciso sobre a política de segurança e fornecer a opção de executar modelos de formulário de código gerenciado do InfoPath como formulários totalmente confiáveis da Intranet, o InfoPath implementa a seguinte arquitetura de segurança.
  
- O aplicativo InfoPath hospeda o CLR (Common Language Runtime) do .NET Framework.
    
- No CLR hospedado pelo InfoPath, cada modelo de formulário de código gerenciado é executado em um domínio de aplicativo separado, que é um ambiente que fornece limites de isolamento, descarregamento e segurança para executar código gerenciado.
    
- O InfoPath define uma política de segurança padrão no domínio do aplicativo, dependendo do nível de confiança associado ao modelo de formulário e da URL de seu local.
    
- Por padrão, um modelo de formulário de código gerenciado em execução no computador local (o grupo de códigos da Zona do Meu Computador) obtém um nível inferior de permissões do que Confiança Total (permissões de Zona da Intranet Local). Para ter permissões de Confiança Total, o formulário deve ser registrado ou assinado digitalmente com um certificado confiável.
    
A política de segurança padrão definida para o domínio do aplicativo de um modelo de formulário de código gerenciado garante que os níveis de segurança de acesso ao domínio do InfoPath, bem como quaisquer restrições de segurança adicionais do .NET sejam impostas. Para fornecer flexibilidade adicional, o sistema de segurança do InfoPath reconhece um grupo de códigos de segurança de acesso ao código .NET chamado "Modelos de Formulário do InfoPath". Se esse grupo de códigos estiver presente no computador de um usuário, sua configuração de segurança e as de qualquer grupo de códigos filho dentro dele serão aplicadas ao domínio do aplicativo.
  
> [!IMPORTANT] 
> - O grupo de códigos de Modelos de Formulário do InfoPath só se aplica ao próprio assembly de código de formulário de código gerenciado. Como resultado, se você conceder a permissão Confiança Total definida como código de formulário de código gerenciado do InfoPath, mas não tiver instalado e registrado (ou assinado digitalmente) o modelo de formulário em si (o que torna todo o modelo de formulário totalmente confiável), as chamadas no código do formulário para membros do modelo de objeto de nível 3 de segurança ainda falharão.   
> - Se você referenciar ou carregar explicitamente (Assembly.Load) um assembly configurado com um conjunto de permissões restritas usando evidências de Hash, Nome Forte ou Publisher para determinar sua condição de associação em um projeto de modelo de formulário, o assembly será carregado e executado pelo modelo de formulário.
    
Para obter informações sobre como criar e configurar o grupo de códigos de Modelos de Formulário do InfoPath, consulte Definir configurações de segurança para modelos de [formulário com código.](how-to-configure-security-settings-for-form-templates-with-code.md)
  
A tabela a seguir resume os cenários de implantação e conjuntos de permissões que se aplicam aos modelos de formulário de código gerenciado.
  
|**Cenário de implantação**|**Conjunto de Permissões**|**Anotações**|
|:-----|:-----|:-----|
|O modelo de formulário é publicado no computador local e o desenvolvedor está usando o Visual Studio para escrever e depurar o código do formulário.  <br/> |Conjunto de permissões da Intranet Local.  <br/> Os assemblies instalados no GaC (Cache de Assembly Global) e marcados com o atributo **AllowPartiallyTrustedCallersAttribute** são concedidos com o conjunto de permissões Confiança Total.  <br/> |Por padrão, modelos de formulário em execução no computador local não são concedidos com o conjunto de permissões Confiança Total. Ao desenvolver modelos de formulário que usam recursos e chamadas para membros do modelo de objeto que exigem permissões de Confiança Total, você pode usar o procedimento descrito em Visualizar e [Depurar](how-to-preview-and-debug-form-templates-that-require-full-trust.md)Modelos de Formulário que Exigem Confiança Total .  <br/> |
|O modelo de formulário é publicado no computador local e faz referência a um assembly personalizado que solicita o conjunto de permissões Confiança Total no computador local.  <br/> |Conjunto de permissões da Intranet Local.  <br/> Os assemblies instalados no GaC (Cache de Assembly Global) e marcados com o atributo **AllowPartiallyTrustedCallersAttribute** são concedidos com o conjunto de permissões Confiança Total. O assembly personalizado é concedido ao conjunto de permissões da Intranet Local.  <br/> |Para fazer referência a assemblies externos para uso no código do modelo de formulário, o desenvolvedor deve usar o grupo de códigos de Modelos de Formulário do InfoPath para conceder Confiança Total (ou o conjunto de permissões apropriado) ao assembly externo referenciado no código do modelo de formulário. O InfoPath não faz suposições sobre assemblies externos que não os instalados no CACHE de Assembly Global (GAC). O desenvolvedor deve conceder explicitamente ao assembly as permissões necessárias usando o grupo de códigos de Modelos de Formulário do InfoPath, mesmo se o assembly já for confiável, embora as permissões concedidas no grupo My_Computer_Zone código.  <br/> |
|O modelo de formulário é publicado em um local compartilhado na intranet local, como um compartilhamento de arquivos, uma biblioteca de formulário do SharePoint ou um servidor Web.  <br/> |Conjunto de permissões da Intranet Local.  <br/> Os assemblies instalados no GaC (Cache de Assembly Global) e marcados com o atributo **AllowPartiallyTrustedCallersAttribute** são concedidos com o conjunto de permissões Confiança Total.  <br/> ||
|O modelo de formulário é publicado em um local compartilhado na intranet local, como um compartilhamento de arquivos, uma biblioteca de formulário do SharePoint ou um servidor Web designado como um site confiável no Internet Explorer.  <br/> |Conjunto de permissões da Internet.  <br/> Os assemblies assinados pela Microsoft e pelo ECMA são concedidos com o conjunto de permissões Confiança Total.  <br/> |A segurança de acesso ao código CLR concede apenas o conjunto de permissões de Internet para sites designados como sites confiáveis no Internet Explorer. O InfoPath respeita essa política. Observe que isso é diferente de um modelo de formulário do InfoPath que usa script para código de formulário, que recebe um nível mais alto de permissões quando publicado em uma zona de sites confiáveis.  <br/> |
|O modelo de formulário é baixado ou copiado de um local da Internet.  <br/> |Por padrão, nenhum. O assembly de código gerenciado para o modelo de formulário não é carregado e não é executado.  <br/> ||
   
## <a name="see-also"></a>Confira também

- [Definir configurações de segurança para modelos de formulário com código](how-to-configure-security-settings-for-form-templates-with-code.md)
- [Visualizar e depurar modelos de formulário que exigem confiança total](how-to-preview-and-debug-form-templates-that-require-full-trust.md)

