class NameForm extends React.Component {
  constructor(props) {
    super(props);
    this.state = { value: '' };
    this.handleChange = this.handleChange.bind(this);
    this.handleSubmit = this.handleSubmit.bind(this);
  }
  handleChange(event) {
    this.setState({ value: event.target.value });
  }
handleSubmit(event) {
    alert('A name was submitted: ' + this.state.value);
    event.preventDefault();
  }




  render() {
    return (
      <form onSubmit={this.handleSubmit}>
        <label>
          Name:
          <input type="text" value={this.state.value}     
                      onChange={this.handleChange} />
        </label>
        <button type="submit">Submit</button>
      </form>
    );
  }
}

![image](https://github.com/user-attachments/assets/446b16ea-e652-4370-83b2-28a2d18d3983)
