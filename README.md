<html>
  <h2>Generate Fake Data</h2>
  <p>This script uses the <a href="https://github.com/stympy/faker">faker</a> gem
     to generate fake data files.
  </p>
  <h3>Installation</h3>
  <p>
      Download zip of files and unpack. Make sure you have
      <a href="https://github.com/bundler/bundler">bundler</a> installed. Then
      at the directory head where you installed type: bundle install
  </p>
  <h3>Usage</h3>
  <p style="font-size:14px"><font face="Courier New">ruby gen_fake_data -c [config_file.yml]</font></p>
  <h3>Configuration</h3>
  <p>
    The structure of the generated file can be set using an inputted YAML
    configuration file. A sample config file is included in the project.
  </p>
  <h4>Config File Parameters:</h4>
  <table border="1" style="width:70%">
    <tr>
      <th>Value</th>
      <th>Description</th>
    </tr>
    <tr>
      <td>num_transactions</td>
      <td>The number of rows to be in the output file</td>
    </tr>
    <tr>
      <td>band_data</td>
      <td>Should the script band the file, yes or no?</td>
    </tr>
    <tr>
      <td>outfile</td>
      <td>The name of the output file</td>
    </tr>
    <tr>
      <td>bands_file</td>
      <td>Use a bands file if banding, yes or no?</td>
    </tr>
    <tr>
      <td>bands_filename</td>
      <td>Name of bands file for bandit to use if banding</td>
    </tr>
    <tr>
      <td>dependent</td>
      <td>Use dependent if banding, yes or no?</td>
    </tr>
    <tr>
      <td>dependent_cat</td>
      <td>Dependent category if banding</td>
    </tr>
  </table>
  <h4>Config File Parameter columns:</h4>
  <p>
     Each yaml array entry for the columns parameter defines category columns for
     the output file. With a few exceptions these correspond to faker data types.
     Category corresponds to a faker class while the type is the method. Not all
     faker Classes are supported yet but can be added as needed.
  </p>
  <p>
    For example, a category entry as follows:
  </p>
  <p>
    <font color="blue">columns</font>:<br>
    - <font color="blue">name</font>: Customer<br>
    &nbsp;&nbsp;<font color="blue">category</font>: Name<br>
    &nbsp;&nbsp;<font color="blue">type</font>: name<br>
  </p>
  <p>
    Corresponds to <b>Faker::Name.name</b> and would create a column in the output file
    with the header name "Customer".
  </p>
  <h4>Non-Faker Categories</h4>
  <p>There are a few non-faker categories supported. More can be added as needed.</p>
  <table border="1" style="width:70%">
    <tr>
      <th>Category</th>
      <th>Type</th>
    </tr>
    <tr>
      <td>Binary</td>
      <td>txt - true/false; num - 0/1</td>
    </tr>
    <tr>
      <td>Date</td>
      <td>e.g. - 10/30/81</td>
    </tr>
  </table>
</html>

