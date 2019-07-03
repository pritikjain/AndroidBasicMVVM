# AndroidBasicMVVM
MVVM stands for Model, View, ViewModel.

Model: This holds the data of the application. It cannot directly talk to the View. Generally, it’s recommended to expose the data to the ViewModel through Observables.
View: It represents the UI of the application devoid of any Application Logic. It observes the ViewModel.
ViewModel: It acts as a link between the Model and the View. It’s responsible for transforming the data from the Model. It provides data streams to the View. It also uses hooks or callbacks to update the View. It’ll ask for the data from the Model.


https://cdn.journaldev.com/wp-content/uploads/2018/04/android-mvvm-pattern.png

There are two ways to implement MVVM in Android:

Data Binding
RXJava

Here be using Data Binding only.
Data Binding Library was introduced by Google in order to bind data directly in the xml layout. For more info on Data Binding, refer this tutorial.

We’ll be creating a simple Login Page Example Application that asks for user inputs. We’ll see how the ViewModel notifies the View when to show a Toast Message without keeping a reference of the View.


How is it possible to notify some class without having a reference of it?

It can be done in three different ways:

Using Two Way Data Binding
Using Live Data
Using RxJava


Two Way Data Binding

Two-way Data Binding is a technique of binding your objects to your XML layouts such that the Object and the layout can both send data to each other.

In our case, the ViewModel can send data to the layout and also observe changes.

For this, we need a BindingAdapter and custom attribute defined in the XML.

The Binding Adapter would listen to changes in the attribute property.

We’ll learn more about Two-way Data Binding through our example below.
