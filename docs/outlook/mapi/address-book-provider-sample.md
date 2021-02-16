---
title: Exemplo de provedor de agenda de endereços
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 2ccf1643-5604-4fee-92cc-3d6af00e7f98
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: fa2a447d0757e75c95d7dc3d9b1dd16b8c7a8084
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331105"
---
# <a name="address-book-provider-sample"></a>Exemplo de provedor de agenda de endereços

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Este exemplo dá suporte a um único contêiner somente leitura para exibir nomes e endereços de email, que são lidos de um arquivo binário simples. O exemplo oferece suporte a modelos one-off e todas as opções de configuração, exceto o Assistente de Perfil.
  
Você pode baixar este exemplo dos exemplos de código [da API de Mensagens do Outlook (MAPI).](https://go.microsoft.com/fwlink/?LinkId=129740
)
  
|||
|:-----|:-----|
|Executável:  <br/> |SABP32.dll  <br/> |
| Diretório do código-fonte:  <br/> |SampleAddressBookProvider\SABP  <br/> |
|Idioma:  <br/> |C++  <br/> |
|Plataformas:  <br/> |Microsoft Visual Studio 2008 para compilar para Windows Vista, Windows Server 2008, Windows XP SP2 e Windows Server 2003 SP1  <br/> |
   
## <a name="supported-features"></a>Recursos com suporte

Este exemplo dá suporte aos seguintes recursos:
  
- Restrições de tabela. O exemplo implementa a resolução de prefixo e nome ambíguo. Ele não implementa a linguagem de restrição MAPI completa e as restrições são suportadas apenas no nome de exibição.
    
- Uma tabela de exibição de detalhes para usuários de mensagens. 
    
- Endereços one-off.
    
- Uma caixa de diálogo de pesquisa avançada.
    
- Uma [interface IMAPIStatus : IMAPIProp.](imapistatusimapiprop.md) Essa interface é parcialmente suportada; seus **métodos IMAPIProp** são delegados à interface **IPropData.** Para obter mais informações, consulte a interface [IPropData : IMAPIProp.](ipropdataimapiprop.md) 
    
- Configuração interativa e programática.
    
## <a name="unsupported-features"></a>Recursos sem suporte

Este exemplo não dá suporte aos seguintes recursos:
  
- Classificação.
    
- Listas de distribuição.
    
- Criação, exclusão e modificação de entradas.
    
- Propriedades com vários valores.
    
- Propriedades nomeadas.
    
- Distinção entre o nome e o sobrenome em nomes de exibição.
    
 **Para instalar o Provedor de Lista de Endereços de Exemplo**
  
1. Para baixar o Provedor de Livro de Endereços de Exemplo, consulte [Baixando os exemplos de MAPI do Outlook.](downloading-the-outlook-mapi-samples.md)
    
2. Localize a pasta onde você salvou os exemplos de MAPI do Outlook. Clique com o botão direito do mouse na pasta zip do número de versão do **OutlookMAPISamples \< \>** e clique em **Extrair Tudo.**
    
3. Clique **em** Procurar, selecione o local onde deseja salvar o exemplo e clique em **Extrair.**
    
4. Execute o Visual Studio 2008.
    
5. No Visual Studio 2008, clique em **Arquivo,** selecione **Abrir** e clique em **Projeto/Solução.**
    
6. Navegue até o local onde você salvou o exemplo, clique **em SABP.vcproj** e, em seguida, clique em **Abrir**.
    
7. On the **Build** menu, click **Build Solution**.
    
8. Na caixa **de diálogo Salvar Arquivo como,** clique em **Salvar.**
    
9. Na pasta onde você salvou o exemplo, clique com o botão direito do mouse no **arquivoinstall.bat** e clique em **Executar como administrador.**
    
10. Na caixa de diálogo **Controle de Conta de Usuário**, clique em **Continuar**.
    
    > [!NOTE]
    > **Install.bat** copia a .dll para a pasta de instalação padrão do Microsoft Office, C:\Arquivos de Programas\Microsoft Office\Office12\. Se você instalou produtos do Office em um local diferente, clique com o botão direito do mouse **Install.bat** e clique em **Editar.** O arquivo é aberto no Bloco de Notas. Substitua o caminho de instalação padrão pelo caminho de instalação usado no computador. 
  

