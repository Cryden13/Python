# Scrolled Frame

This ScrolledFrame Widget behaves like a tk.Frame widget but also has vertical  
and/or horizontal scroll bars. The bars can be on either edge of the widget,  
and can be set to disappear automatically when not needed.

## Usage

- `ScrolledFrame` ( master [, scrollbars, padding, dohide, doupdate, scrollspeed, **kwargs])

  The constructor accepts all tk.Frame widget keyword arguments, plus the following
  special immutable arguments:

## Special Arguments

### scrollbars

1. ### `scrollbars` _(optional)_

   **String** _(default="SE")_  
   Where to put the scrollbars (e/g "SR"=South and Right edges).  
   Must be with 1 or 2 characters.

2. ### `padding` _(optional)_

   **Integer OR list of integers** _(default=[3,0,0,3])_  
   Padding between the outer tk.Frame/Scrollbars and the inner tk.Frame.  
   One of: int(pad_all) *OR* list(pad_NS, pad_EW) *OR* list(pad_top, pad_right, pad_bottom, pad_left)

3. ### `dohide` _(optional)_

   **Boolean** _(default=True)_  
   Whether to hide the scrollbars when not needed.

4. ### `doupdate` _(optional)_

   **Boolean** _(default=True)_  
   Whether to automatically redraw the Widget whenever it changes size.  
   Setting to False may improve performance.

5. ### `scrollspeed` _(optional)_

   **Integer** _(default=2)_  
   The number of lines to scroll by per mousewheel scroll.  
   Setting to 0 disables mousewheel scrolling

## Accessible Data Members

- **Outer tk.Frame** _(name=container)_
- **Scrollbars** _(name=vScrbar & hScrbar)_
- **Canvas** _(name=scrollCanvas)_

## Options and Methods

Configuration options are passed to the inner tk.Frame widget, along with most  
method calls; however, geometry methods are redirected to the outer Frame widget.  

The Class also has a special function `redraw` which will update the Widget's  
scroll area and hide/unhide the scrollbars (if set).

## Changelog

<table>
    <tbody>
        <tr>
            <th align="center">Version</th>
            <th align="left">Changes</th>
        </tr>
        <tr>
            <td align="center">1.0</td>
            <td>Initial release</td>
        </tr>
        <tr>
            <td align="center">1.1</td>
            <td>
                <dl>
                    <dt>new</dt>
                    <ul>
                        <li>added option to move scrollbars</li>
                    </ul>
                    <dt>bugfixes</dt>
                    <ul>
                        <li>fixed incorrect method redirect</li>
                        <li>fixed description</li>
                    </ul>
                </dl>
            </td>
        </tr>
        <tr>
            <td align="center">1.2</td>
            <td>
                <dl>
                    <dt>new</dt>
                    <ul>
                        <li>added ability to toggle hiding</li>
                        <li>added padding option</li>
                        <li>added validation</li>
                    </ul>
                    <dt>bugfixes</dt>
                    <ul>
                        <li>fixed bg and cursor options</li>
                    </ul>
                </dl>
            </td>
        </tr>
        <tr>
            <td align="center">2.0</td>
            <td>
                <dl>
                    <dt>new</dt>
                    <ul>
                        <li>changed main class to inner frame</li>
                        <li>added auto updating and the option to toggle said auto updating</li>
                        <li>added access to data members</li>
                        <li>added mousewheel binding</li>
                        <li>added redraw function</li>
                        <li>consolidated redundant functions</li>
                        <li>removed unnecessary tk.frame</li>
                    </ul>
                    <dt>bugfixes</dt>
                    <ul>
                        <li>fixed validation</li>
                        <li>fixed faulty tagging</li>
                    </ul>
                </dl>
            </td>
        </tr>
        <tr>
            <td align="center">2.1</td>
            <td>
                <dl>
                    <dt>new</dt>
                    <ul>
                        <li>added scrollspeed argument</li>
                        <li>cleaned up code</li>
                        <li>added a bunch of comments</li>
                    </ul>
                    <dt>bugfixes</dt>
                    <ul>
                        <li>fixed lag when updating list</li>
                    </ul>
                </dl>
            </td>
        </tr>
        <tr>
            <td align="center">2.2</td>
            <td>
                <dl>
                    <dt>new</dt>
                    <ul>
                        <li>added typing hints</li>
                    </ul>
                    <dt>bugfixes</dt>
                    <ul>
                        <li>fixed redraw error</li>
                    </ul>
                </dl>
            </td>
        </tr>
    </tbody>
</table>
