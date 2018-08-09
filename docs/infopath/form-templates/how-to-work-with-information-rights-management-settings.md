---
title: Trabalhar com configurações do Gerenciamento de Direitos de Informação
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
keywords:
- gerenciamento de direitos de informação [infopath 2007], IRM do InfoPath 2007, gerenciamento de direitos de informação, [InfoPath 2007]
localization_priority: Normal
ms.assetid: 4ad91898-b23e-4410-8839-a65259e53d37
description: 'Há dois tipos de configurações de gerenciamento de direitos de informação (IRM) disponíveis no Microsoft InfoPath: um para proteger o acesso aos modelos de formulário do InfoPath e outro para controlar o acesso aos e ações nos dados do formulário contidos em formulários preenchidos.'
ms.openlocfilehash: 4e6fdac6a0b2b5cd6a29de948cc9dbbd01a407d8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765644"
---
# <a name="work-with-information-rights-management-settings"></a>Trabalhar com configurações do Gerenciamento de Direitos de Informação

Há dois tipos de configurações de gerenciamento de direitos de informação (IRM) disponíveis no Microsoft InfoPath: um para proteger o acesso aos modelos de formulário do InfoPath e outro para controlar o acesso aos e ações nos dados do formulário contidos em formulários preenchidos.
  
> [!NOTE]
> Restringindo permissão só está disponível para modelos de formulário compatíveis com o editor do InfoPath. Modelos de formulário compatíveis com navegador não suportam o IRM. 
  
## <a name="adding-the-manage-credentials-command-to-the-quick-access-toolbar"></a>Adicionando o comando de credenciais de gerenciar na barra de ferramentas de acesso rápido

O comando **Gerenciar credenciais** usado para trabalhar com configurações de IRM durante a criação de um modelo de formulário não está disponível por padrão. Use as seguintes etapas para adicioná-lo à barra de **Ferramentas de acesso rápido**.
  
### <a name="add-the-manage-credentials-command-to-the-quick-access-toolbar"></a>Adicione o comando de credenciais de gerenciar na barra de ferramentas de acesso rápido

1.  Clique na seta na extremidade direita da barra de **Ferramentas de acesso rápido** para baixar os menu **Personalizar ferramentas de acesso rápido** e, em seguida, clique em **Mais de comandos**.
    
2. Na lista **Escolher comandos em** , selecione **Todos os comandos**.
    
3. Percorra a lista para **Gerenciar credenciais**e, em seguida, clique em **Adicionar**.
    
4. Clique em **OK**.
    
Para obter mais informações sobre o uso de **Credenciais de gerenciar** comando e a caixa de diálogo **permissão** caixa no InfoPath, consulte o tópico "Criar um formulário modelo com permissão restrita" na Ajuda do InfoPath. 
  
## <a name="the-irm-object-model"></a>O modelo de objeto do IRM

Use a classe de [permissão](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Permission.aspx) para acessar as configurações de permissão [UserPermissionCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.UserPermissionCollection.aspx) e IRM que podem ser aplicadas a um formulário. Para acessar o objeto de **permissão** associado a um modelo de formulário, use a propriedade [Permission](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Permission.aspx) da classe [XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) . O objeto retornado da **permissão** fornece acesso à coleção de objetos [UserPermission](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.UserPermission.aspx) associados com o modelo de formulário e cada instância do formulário criado com esse modelo. 
  
Objeto **Permission** e suas propriedades e métodos estão disponíveis se as permissões são restritas no modelo de formulário ativo ou não. Use a propriedade [Enabled](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Permission.Enabled.aspx) para determinar se um formulário possui permissões restritas. 
  
Usando propriedades e métodos da classe permissão, permissões em um formulário são habilitadas em uma das seguintes maneiras:
  
A propriedade **Enabled** é definida como **true**.
  
A propriedade [DocumentAuthor](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Permission.DocumentAuthor.aspx) é definida. 
  
A propriedade [RequestPermissionUrl](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Permission.RequestPermissionUrl.aspx) estiver definida. 
  
A propriedade [StoreLicenses](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Permission.StoreLicenses.aspx) é definida como **true** ou **false**.
  
O método [ApplyPolicy](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Permission.ApplyPolicy.aspx) é chamado. 
  
> [!NOTE]
> Se o cliente Windows Rights Management não está instalado no computador de um usuário, usando a classe de **permissão** levanta uma exceção. 
  
Para trabalhar programaticamente com as configurações de IRM de usuários individuais em formulários, use as classes **UserPermissionCollection** e **UserPermission** . 
  
Um objeto **UserPermission** associa um conjunto de permissões para o formulário atual com um único usuário e uma data de vencimento opcional. Use o método [Add](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.UserPermissionCollection.Add.aspx) da classe **UserPermissionCollection** para adicionar e conceder a um usuário um conjunto de permissões no formulário atual. Use o método [Remove](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.UserPermissionCollection.Remove.aspx) da classe **UserPermissionCollection** para remover um usuário e as permissões do usuário. Enquanto algumas permissões concedidas através da interface do usuário se aplicam a todos os usuários, como a data de expiração e de impressão, você pode usar as classes **UserPermission** e **UserPermissionCollection** para atribuí-las em uma base por usuário com por usuário datas de expiração. O modelo de objeto permite aos desenvolvedores para enumerar as configurações de permissão em um formulário e fornecem funcionalidade que permite que os usuários do formulário Adicionar permissões ao formulário sem precisar usar o painel de tarefas de **Permissão do formulário** ou caixa de diálogo **permissão** . 
  
> [!NOTE]
> Permissões não podem ser aplicadas quando um formulário está no modo de visualização. Por esse motivo, todas as propriedades da classe **permissão** são somente leitura quando um formulário está sendo visualizado. No modo de visualização, a propriedade **Enabled** sempre retornará **false**e se o código tentar alterar essa configuração, um **System.Runtime.InteropServices.COMException** é gerado e o erro "o método/propriedade não está disponível no modo de visualização modo"é retornado. Da mesma forma, os métodos associados as classes **UserPermission** e **UserPermissionCollection** também retornará essa mensagem de erro quando usado no modo de visualização. 
  
### <a name="overview-of-the-permission-class"></a>Visão geral da classe permissão

A classe **UserPermissionCollection** fornece as seguintes propriedades e um método. 
  
|**Nome**|**Descrição**|
|:-----|:-----|
|Método [ApplyPolicy](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Permission.ApplyPolicy.aspx)  <br/> |Aplica uma diretiva para o formulário usando um arquivo de modelo de política.  <br/> |
|Propriedade [DocumentAuthor](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Permission.DocumentAuthor.aspx)  <br/> |Obtém ou define o autor do formulário atual como um endereço de email.  <br/> |
|Propriedade [Enabled](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Permission.Enabled.aspx)  <br/> |Obtém ou define se as configurações de permissão representadas pelo objeto de **permissão** estão habilitadas para o formulário atual.  <br/> |
|Propriedade [PermissionFromPolicy](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Permission.PermissionFromPolicy.aspx)  <br/> |Obtém ou define se uma política de permissão foi aplicada ao formulário atual.  <br/> |
|Propriedade [PolicyDescription](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Permission.PolicyDescription.aspx)  <br/> |Obtém uma descrição da política que foi aplicada ao formulário atual.  <br/> |
|Propriedade [PolicyName](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Permission.PolicyName.aspx)  <br/> |Obtém o nome da política que foi aplicado ao formulário atual.  <br/> |
|Propriedade [RequestPermissionUrl](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Permission.RequestPermissionUrl.aspx)  <br/> |Obtém ou define o arquivo, URL ou endereço de email de contato para usuários que precisam de permissões adicionais no formulário atual.  <br/> |
|Propriedade [StoreLicenses](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Permission.StoreLicenses.aspx)  <br/> |Obtém ou define se a licença do usuário para exibir o formulário atual deve ser armazenados em cache para permitir a exibição offline quando o usuário não pode se conectar a um servidor de gerenciamento de direitos.  <br/> |
|Propriedade [permissõesde usuário](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Permission.UserPermissions.aspx)  <br/> |Obtém um objeto **UserPermissionCollection** para o formulário atual.  <br/> |
   
### <a name="overview-of-the-userpermissioncollection-class"></a>Visão geral da classe UserPermissionCollection

A classe **UserPermissionCollection** fornece as seguintes propriedades e métodos. 
  
|**Nome**|**Descrição**|
|:-----|:-----|
|Método [Add](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.UserPermissionCollection.Add.aspx) (sobrecargas + 3)  <br/> |Adiciona um novo usuário ao formulário atual, opcionalmente, especificando permissões e uma data de validade.  <br/> |
|Método [Remove](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.UserPermissionCollection.Remove.aspx)  <br/> |Remove o objeto **UserPermission** com o especificado **UserId** da coleção.  <br/> |
|Método [RemoveAll](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.UserPermissionCollection.RemoveAll.aspx)  <br/> |Remove todos os objetos **UserPermission** da coleção.  <br/> |
|Propriedade [Count](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.UserPermissionCollection.Count.aspx)  <br/> |Obtém o número de objetos **UserPermission** da coleção.  <br/> |
|Propriedade [item](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.UserPermissionCollection.Item.aspx) (sobrecarga + 1)  <br/> |Obtém um objeto **UserPermission** .  <br/> |
   
### <a name="overview-of-the-userpermission-class"></a>Visão geral da classe UserPermission

A classe **UserPermission** fornece as seguintes propriedades e um método. 
  
|**Nome**|**Descrição**|
|:-----|:-----|
|Método [Remove](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.UserPermission.Remove.aspx)  <br/> |Remove o objeto **UserPermission** atual de permissões do formulário.  <br/> |
|Propriedade [ExpirationDate](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.UserPermission.ExpirationDate.aspx)  <br/> |Obtém ou define a data de vencimento opcional para as permissões no formulário atual atribuído ao usuário associado a uma instância da classe **UserPermission** .  <br/> |
|Propriedade [Permission](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.UserPermission.Permission.aspx)  <br/> |Obtém ou define um valor que representa as permissões no formulário atual atribuído ao usuário associado a uma instância da classe **UserPermission** .  <br/> |
|Propriedade [UserId](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.UserPermission.UserId.aspx)  <br/> |Obtém o endereço de email do usuário cujas permissões no formulário atual são determinadas pelo objeto **UserPermission** especificado.  <br/> |
   
### <a name="the-permissiontype-enumeration"></a>A enumeração PermissionType

Permissões de um usuário são definidas ou lido usando valores de enumeração [PermissionType](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.PermissionType.aspx) . 
  
|**Nome**|**Descrição**|
|:-----|:-----|
|**PermissionType.Change** <br/> |Permite aos usuários exibir, editar, copiar e salvar, mas não imprimir um formulário. Equivalente à **leitura**, as permissões **Editar**, **Salvar**e **extrair** combinadas.  <br/> |
|**PermissionType.Edit** <br/> |Permite que o usuário edite o formulário.  <br/> |
|**PermissionType.Extract** <br/> |Permite que um usuário com a permissão de **leitura** copiem o conteúdo no formulário.  <br/> |
|**PermissionType.FullControl** <br/> |Permite ao usuário adicionar, alterar e remover permissões para outros usuários de um formulário.  <br/> |
|**PermissionType.ObjectModel** <br/> |Permite que um usuário acessar o documento de formulário de forma programática por meio de seu modelo de objeto. Os usuários sem a permissão **ObjectModel** não podem usar o modelo de objeto para determinar suas próprias permissões.  <br/> |
|**PermissionType.Print** <br/> |Permite ao usuário imprimir o formulário.  <br/> |
|**PermissionType.Read** <br/> |Permite ao usuário ler (exibição) o formulário. (As permissões de **leitura** e o **modo de exibição** são equivalentes).  <br/> |
|**PermissionType.Save** <br/> |Permite que o usuário salve o formulário.  <br/> |
|**PermissionType.View** <br/> |Permite ao usuário exibir (leitura) do formulário. (As permissões de **leitura** e o **modo de exibição** são equivalentes).  <br/> |
   
### <a name="example"></a>Exemplo

No exemplo a seguir, clicando no controle de **botão** obtém o **UserPermissionsCollection** para o formulário atual, adiciona e atribui um usuário para o nível de acesso de alteração e define uma data de validade de dois dias a partir da data atual. 
  
```cs
public void CTRL1_Clicked(object sender, ClickedEventArgs e)
{
   string strExpirationDate = DateTime.Today.AddDays(2).ToString();
   DateTime dtExpirationDate = DateTime.Parse(strExpirationDate);
   this.Permission.UserPermissions.Add("someone@example.com", 
      PermissionType.Change, dtExpirationDate);
}
```

```vb
Public Sub CTRL1_Clicked(ByVal sender As Object, _
   ByVal e As ClickedEventArgs)
   Dim strExpirationDate As String = _
      DateTime.Today.AddDays(2).ToString()
   dtExpirationDate As DateTime = DateTime.Parse(strExpirationDate)
   Me.Permission.UserPermissions.Add("someone@example.com", _
      PermissionType.Change, dtExpirationDate)
End Sub
```


