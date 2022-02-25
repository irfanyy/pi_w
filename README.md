<h2>Intro</h2>
    <p>Our goal is to create simple user management screens. This document contains information about this. It is an information document about the details of the screens, their requirements and how they should be.</p>

<h2>Who's for it?</h2>
    <p>This system appeals to the panel user who is authorized to view and add all users.</p>

<h2>Why build it?</h2>
    <p>Our panel user should be able to quickly and easily add, filter, sort and view inactive users by hiding them. That's why we want to create and present this panel in the most effective way. We are preparing two separate screens.</p>

<h2>What is it?</h2>
    <ol>
        <li>
            <h4>Index View</h4>
                <p>The Index View (ie, homepage) displays the list of users id, user name, email, enabled segmented. (Logged in).
                CTA must be sent for login when not logged in.</p>
        </li>
        <li>
            <h4> Screens </h4>
                <ul>
                    <li> 
                        <h6> Add User </h6>
                        <p>This screen should allow us to add users. On this screen, there should be necessary and optional inputs for the user, a select to determine the role, a checkbox to determine whether it is active or passive, and a registration button that sends this information.</p>
                    </li>
                    <li> 
                        <h6> View Users </h6>
                        <p>We should be able to see all users on this screen in tabular form. For this table to be prepared as a datatable, the tables must be sortable and a filtering feature must be added for each table. On this screen, there should be a new registration button that allows us to go to the screen that adds a new user. On the right of the button, we should be able to hide inactive users by adding checkbox and disabled.</p>
                    </li>
                </ul>
        </li>
        <li>
            <h4> Glossary </h4>
            <ul>
                <li> user_name: for user name inputs key </li>
                <li> display_name: for display name inputs key </li>
                <li> email: email input key </li>
                <li> phone: phone input key </li>
                <li> user_role: user roles selectable key </li>
                <li> enabled_disabled: enable checkbox key </li>
            </ul>
        </li>
        <li> 
            <h4> Components </h4>
            <ul>
                <li> Add User Screen Components
                    <ol>
                        <li> Labels (for inputs left side)
                                <ul>
                                    <li> User name input => [Username:] </li>
                                    <li> Display Name input => [Display Name:] </li>
                                    <li> Phone input => [Phone:] </li>
                                    <li> E-mail input => [Email:] </li>
                                    <li> User Roles Select => [User Roles:] </li>
                                    <li> Enable/Disable Checkbox => [Enabled] </li>
                                    <li> Save user Button => [Save User] </li>
                                </ul>
                        </li>
                        <li> Inputs
                            <ul>
                                <li> User name </li>
                                <li> Display name </li>
                                <li> Phone </li>
                                <li> E-mail </li>
                            </ul>
                        </li>
                        <li> Select
                            <ul>
                                <li> User Roles Options
                                    <ol>
                                        <li> Guest </li>
                                        <li> Admin </li>
                                        <li> Super Admin </li>
                                    </ol>
                                </li>
                            </ul>
                        </li>
                        <li> Checkbox
                            <ul>
                                <li> Status 
                                    <ol>
                                        <li>if check Enabled not checked disabled user</li>
                                    </ol>
                                </li>
                            </ul>
                        </li>
                        <li> Buttons
                            <ol>
                                <li>Save User button.</li>
                            </ol>
                        </li>
                    </ol>
                </li>
                <li> View Users Components
                    <ol>
                        <li> Datatable
                            <p>On this screen, the column headers should be blue and the icons next to them (filter and sort icons). In the lists, there should be white and gray coloring with the zipper method.</p>
                            <ul>
                                <li> ID (sortable, filter) </li>
                                <li> Username (sortable, filter) </li>
                                <li> Email (sortable, filter) </li>
                                <li> Enabled (sortable, filter) </li>
                            </ul>
                        </li>
                        <li> Labels
                            <ul>
                                <li> Checkbox Label => [Hide Disabled User] </li>
                                <li> New user button => [Icon[+] New User] </li>
                            </ul>
                        </li>
                        <li> Checkbox
                            <ul>
                                <li> if check hide all disabled user, not check display all user </li>
                            </ul>
                        </li>
                    </ol>
                </li>
            </ul>
        </li>
        <li>
            <h4> Validations </h4>
            <ul>
                <li> Add User Screen Validations
                    <ol>
                        <li> User name     => required, minimum two string </li>
                        <li> Display name  => required, minimum two string </li>
                        <li> Phone         => required, minimum 10 digits, maximum 11 digits (for turkey) </li>
                        <li> E-mail        => required, check email regex </li>
                        <li> User Roles    => required select </li>
                        <li> Enabled Check => optional, check or not check </li>
                    </ol>
                </li>
            </ul>
        </li>
        <li> 
            <h4> Errors </h4>
            <ul>
                <li> Add User Screen Errors
                    <p>if you get inputs condition errors show error below input: </p>
                    <ol>
                        <li> user_name.required - 'User name required, write please' </li>
                        <li> user_name.digits|min:2 -  'User name must be minimum 2 string, write please' </li>
                        <li> display_name.required: 'Display name required, write please' </li>
                        <li> display_name.digits|min:2 - 'Display name must be minimum 2 string, write please' </li>
                        <li> phone.required - 'Phone is required, please write' </li>
                        <li> phone.digits|min:10|max:11 - 'Phone is minimum 10 digits and 11 maximum digits, write please' </li>
                        <li> email.required|regex - 'Email is required and must be correct, please write', </li>
                        <li> user_role.required - 'You must select user roles, please select an value', </li>
                    </ol>
                </li>
                <li> View Users Screen Errors
                        <p>We don't expect a specific error on this screen, but it will be enough for us to see the message that it is specialized for an error caused by filters, sorting or checkbox, or an error has occurred. We can show this text by writing in red at the top of the page.</p>
                </li>
            </ul>        
        </li>
        <li>
            <h4> Fonts </h4>
                <p>All screen component and text font must be: google-sans</p>
        </li>
        <li>
            <h4> Component Colors </h4>
            <ul>
                <li> Add User Screen Colors
                    <ol>
                        <li> Background is must be White. </li>
                        <li> Please use classic bootstrap colors for inputs </li>
                        <li> Save User button's color is must be light Blue. </li>
                        <li> Select hover value colors is must be light Blue. </li>
                    </ol>
                </li>
                <li> View Users Screen Colors
                    <ol>
                        <li> Columns header is Blue. </li>
                        <li> The list should be one gray and one white. </li>
                        <li> New User Button color must be Blue. </li>
                        <li> Please use classic bootstrap colors for checkbox </li>
                    </ol>
                </li>
                > Blue Code: #5f33e5
                > Light Blue: #9581d1
                > Grey: #d7d7d7
                > White: #fff
            </ul>
        </li>
    </ol>

<h2> Mockups </h2>
    <ul>
        <li> Add User </li>
            ![](/add-user.png)
        <li> View Users </li>
            ![](/view-users.png)
    </ul>